# Intro_to_dMRI_workshop

This repo integrate a previous repo created as part of [ Neuroimaging Carpentry](https://conp-pcno-training.github.io/neuroimaging-carpentry/)  and includes tutorial for working with dMRI data using [DIPY](https://dipy.org/).

## About the Lesson

This lesson teaches:
- What diffusion Magnetic Resonance Imaging is
- How dMRI data is organized within the BIDS framework
- What the standard preprocessing steps in dMRI are
- How local fiber orientation can be reconstructed using dMRI data
- How dMRI can provide insight into structural white matter connectivity

## Local

If users choose to run the `Jupyter` notebooks locally, the following
dependencies will need to be installed:

- [ANTs] : used to register different anatomical data.
- [FSL] : used for different data preprocessing steps.
- [DIPY] : used for diffusion MRI data processing.
- [FURY] : used for anatomical data visualisation purposes.
- [Matplotlib] : used for data visualisation purposes.
- [Nilearn] : used for anatomical data visualisation purposes.
- [osfclient] : used to download the necessary data.
- [PyBIDS] : used to check the data structure [BIDS] compliance.


To run the code locally please follow the instructions:

1) Clone this repo using:
```
git clone https://github.com/Davi1990/Intro_to_dMRI_workshop
```

2) Install the required dependencies using:
```
pip install -r requirements.txt
```

3) Download the necessary data

Notebooks expect them to be placed in the `data` folder that exists in the root
of the repository.

Note that the above command clones the entire repository, which may be quite large and
take a while to download. Alternatively, data from a single subject is available
and can be downloaded by running:
~~~
$ cd ./data
$ osf -p cmq8a fetch ds000221_subject/ds000221_sub-010006.zip
$ unzip ds000221_sub-010006.zip
~~~
{: .language-bash}


## Extra steps

> ## Test the installation
>
> Test installation information for a package can be checked by running, for
> example:
> ~~~
> $ pip show dipy
> ~~~
> {: .language-bash}
>
> Similarly, it can be checked that a given package can be imported in Python by
> running, for example:
> ~~~
> $ python
> >>> import dipy
> ~~~
> {: .language-bash}
>
> Alternatively, the package version can also be checked by running, for example:
> ~~~
> $ python
> >>> import dipy
> >>> print(dipy.__version__)
> ~~~
> {: .language-bash}
>
> You can also see the packages and versions of all `pip`-installed dependencies
> by typing:
> ~~~
> $ pip freeze
> ~~~
> {: .language-bash}
{: .discussion}

In order to run the notebooks, the notebook server needs to be started. Once the
current directory changed to the root of the code directory, the server is
started running:
~~~
$ ipython notebook
~~~
{: .language-bash}

if using `IPython`, and running:

~~~
jupyter-lab
~~~
{: .language-bash}

if using `JupyterLab`.

In either case, the commands will print some information about the notebook
server in the terminal, and a web browser will be opened to the URL of the web
application (by default, http://127.0.0.1:8888). The users will be presented to
the directory structure of the current directory, and they will be able to run
the notebook of interest.

For additional information about `Python` setups besides the package manuals,
users are encouraged to read the [Programming with Python] Carpentries lesson.

The data used in the lesson is hosted in [OSF]. It can be downloaded by running:
~~~
$ osf -p cmq8a clone ./data
~~~
{: .language-bash}
