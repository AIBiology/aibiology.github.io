---
title: Making a Mamba environment for ViT
tags: [python,jupyter,mamba,kernels]
sidebar: home_sidebar
permalink: vit_mamba_setup.html
summary: How to make conda/mamba environment and custom Jupyter kernels on HiPerGator
keywords: jupyter, python, notebooks, mamba, conda, kernel, hipergator
---

So far, we have used the Jupyter Kernels pre-installed and maintained by UFRC. Those have generally worked for most of what we've needed. We had some issues with `seaborn` and I changed a few things here and there to avoid having to install new stuff...but, we've reached a point where we need a combination of Python modules that aren't available in any one kernel.

You will likely have seen (and may have run) suggestions to `pip install`, or within Jupyter `!pip install`, this package or that package. That will generally work...up to a point. There are a few issues with doing `pip install`:

1. If you install a version of a module that is also installed in by UFRC (either now or in the future), your version will take precedence. Your version appears in the the `PYTHON_PATH` before the UFRC installed version. That may be fine *now*, but some time down the road there may be a newer version installed by UFRC for compatibility with something else and your older version still takes precedence and breaks the other module. This can be hard to diagnose when things start failing as you have likely forgotten that you installed the module in the first place.
1. You may want to install something that needs a different version of a module. Sometimes, the unfortunate reality is that two modules cannot co-exist because they require different versions of dependencies. This becomes a challenge to manage with `pip` as there isn't a method to swap active versions.

## Conda and Mamba to the rescue!

<img src='https://mamba.readthedocs.io/en/latest/_static/logo.png' alt='Mamba logo' width='200' align='right'>

`conda` and the newer, faster, drop-in replacement `mamba`, were written to solve some of these issues. They allow you to have different environments and switch between environments when needed. They also make it much easier to report the exact configuration of modules that are needed to run some code, facilitating reproducibility. 

Check out the [UFRC Help page on conda](https://help.rc.ufl.edu/doc/Conda)

I've setup a `vit` environment for the `21_Vision_Transformers.ipynb` notebook.

To do so, I setup my `~/.condarc` to use `/blue/zoo4926/share/conda/` both to get it out of my home directory and to make it shared with everyone in the group:

```bash
channels:
  - conda-forge
  - bioconda
  - defaults
envs_dirs:
  - /blue/zoo4926/share/conda/envs
pkgs_dirs:
  - /blue/zoo4926/share/conda/pkgs
auto_activate_base: false
auto_update_conda: false
always_yes: false
show_channel_urls: false
```

Then I ran:

`mamba create -n vit`

Then to get the tensorflow compiled with the latest CUDA for the A100s:

`mamba install tensorflow==2.7.0=cuda112*`

> **Note:** if you just `mamba install tensorflow`, you will get a version compiled with an older CUDA, which will be ***extremely*** slow...ask me how I know 🤦

Then add in other stuff:

`mamba install jupyterlab transformers huggingface_hub tensorboard ipywidgets datasets pillow matplotlib scikit-learn seaborn kaggle opencv`

And...of course...`tensorflow-addons` is not in conda yet, so I had to `pip install tensorflow-addons`. Same with `vit-keras`. The good thing is, if you `mamba activate vit` and then run `pip install tensorflow-addons` that is installed in the virtual environment.

## Adding the `vit` environment as a Jupyter kernel

Now we need to add this environment as a Jupyter kernel so that we can select this environment to run our notebook.

Again, while UFRC manages the environments that are globally available, you can always add your own. The steps are outlined on the [UFRC Jupyter page](https://help.rc.ufl.edu/doc/Jupyter_Notebooks#Personal_Kernels)

<img src='https://github.com/AIBiology/Jupyter_Content/blob/main/kernels/vit/logo-64x64.png?raw=true' alt='ViT Kernel logo' align='left'>

I have prepared the kernel and it's in the `kernels` folder of the `Jupyter_Content` repo.

In addition to the global kernels, Jupyter will look in your directory `~/.local/share/jupyter/kernels/` for personal kernels.

After pulling the latest version of the repo, open a terminal and run these commands (or use the repo at `/blue/zoo4926/share/Jupyter_Content` as below)

```bash
# Change to the path where you have the Jupyter_Content repo
cd /blue/zoo4926/share/Jupyter_Content/kernels
# Copy the vit folder to ~/.local/share/jupyter/kernels/
cp -r vit ~/.local/share/jupyter/kernels/
```

Now, refresh the Jupyter tab in your browser. You should now have a ViT Kernel in the list of available kernels!
