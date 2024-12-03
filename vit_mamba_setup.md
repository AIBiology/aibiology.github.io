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

1. If you install a version of a package that is also installed in by UFRC (either now or in the future), your version will take precedence. Your version appears in the the `PYTHON_PATH` before the UFRC installed version. That may be fine *now*, but some time down the road there may be a newer version installed by UFRC for compatibility with something else and your older version still takes precedence and breaks the other module. This can be hard to diagnose when things start failing as you have likely forgotten that you installed the module in the first place.
1. You may want to install something that needs a different version of a package. Sometimes, the unfortunate reality is that two packages cannot co-exist because they require different versions of dependencies. This becomes a challenge to manage with `pip` as there isn't a method to swap active versions.

## Conda and Mamba to the rescue!

<img src='https://mamba.readthedocs.io/en/latest/_static/logo.png' alt='Mamba logo' width='200' align='right'>

`conda` and the newer, faster, drop-in replacement `mamba`, were written to solve some of these issues. They allow you to have different environments and switch between environments when needed. They also make it much easier to report the exact configuration of modules that are needed to run some code, facilitating reproducibility.

Check out the [UFRC Help page on conda, mamba and Jupyter kernels](https://help.rc.ufl.edu/doc/Managing_Python_environments_and_Jupyter_kernels)

I've setup a `vit` environment for the `21_Vision_Transformers.ipynb` notebook.


### Steps to setup the `vit` environment

**I have done these steps for you, so you do not need to do them.** They are here as a template for you to follow in the future.

1. Configure your `~/.condarc` to use `/blue/bsc4892/share/conda/` both to get it out of my home directory and to make it shared with everyone in the group. You could use your own `/blue` directory or where ever you want to store the conda environments.

    ```bash
    channels:
      - conda-forge
      - bioconda
      - defaults
    envs_dirs:
      - /blue/zbsc4892/share/conda/envs
    pkgs_dirs:
      - /blue/bsc4892/share/conda/pkgs
    auto_activate_base: false
    auto_update_conda: false
    always_yes: false
    show_channel_urls: false
    ```

1. Create the conda environment:
 
    ````bash
    module load conda # Needed on HiPerGator to load conda
    mamba create -p /blue/bsc4892/share/conda/envs/vit
    ```

1. Activate the new environment:

    ```bash
    mamba activate /blue/zoo4926/share/conda/envs/vit
    ```
 
1. Start by installing python into the environment. We'll specify python 3.10. This will take some time.

    ```bash
    mamba install python==3.10
    ```

1. When you run a mamba command, it will figure out what needs to be installed, and then ask you to confirm the changes. Then it makes the changes.

1. I'm not sure why, but Tensorflow has stopped using `conda`, so we need to use `pip` to install newer versions. To install Tensoflow with GPU support, run:

    ```bash
    python3 -m pip install tensorflow[and-cuda]
    ```

   * This also takes a bit of time.

1. Install other things via `mamba`:

    ```
    mamba install jupyterlab transformers huggingface_hub tensorboard ipywidgets datasets pillow matplotlib scikit-learn seaborn kaggle opencv
    ```

1. There are some other required packages not distributed via `conda`. Install those with `pip` as well.

    ```
    pip install tensorflow-addons vit-keras
    ```

1. Looks like there's a compatability layer needed for newer Keras...

    ```
    pip install tf-keras
    ```
    

## Adding the `vit` environment as a Jupyter kernel

Now we need to add this environment as a Jupyter kernel so that we can select this environment to run our notebook.

Again, while UFRC manages the environments that are globally available, you can always add your own. The steps are outlined on the [UFRC Jupyter page](https://help.rc.ufl.edu/doc/Jupyter_Notebooks#Personal_Kernels)

<img src='https://github.com/AIBiology/Jupyter_Content/blob/main/kernels/vit/logo-64x64.png?raw=true' alt='ViT Kernel logo' align='left'>

I have prepared the kernel and it's in the `kernels` folder of the `Jupyter_Content` repo.

In addition to the global kernels, Jupyter will look in your directory `~/.local/share/jupyter/kernels/` for personal kernels.

After pulling the latest version of the repo, open a terminal and run these commands (or use the repo at `/blue/bsc4892/share/Jupyter_Content` as below)

```bash
# Change to the path where you have the Jupyter_Content repo
cd /blue/bsc4892/share/Jupyter_Content/kernels
# Copy the vit folder to ~/.local/share/jupyter/kernels/
cp -r vit ~/.local/share/jupyter/kernels/
```

Now, refresh the Jupyter tab in your browser. You should now have a ViT Kernel in the list of available kernels!
