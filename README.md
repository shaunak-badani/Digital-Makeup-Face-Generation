# Digital Makeup Face Generation

## Setup

### Method 1 : Setup on ada / hpc
Conda environment on : 
Install conda from [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)
```
conda env create -f dip_conda_env.yml
conda activate dip
```
Start the jupyter notebook after requesting a node:

```
sinteractive
jupyter notebook --no-browser
```
Forward port from node to your computer
```
ssh -N -f -R 8888:localhost:<jupyter notebook port> <local_username>@<local_ip>
```
Find the local_ip assigned to you after starting vpn on your computer : It should be near `tun0`

Then go to `localhost:8888` on your local machine, if the jupyter notebook interface opens up, then the setup is successful.

Request for the password from the almighty, the one and only.

### Method 2 : Pre-configured setup

Who doesn't like a preconfigured setup?
Team members involved in the project can generate a public private ssh key pair.

Ask for your public key to be added to His ada.

Add the following lines to your `~/.ssh/config` file:
```
Host s-ada
Hostname ada.iiit.ac.in
User shaunak
IdentityFile <path_to_priv_key/id_rsa>
```
Then ssh into shaunak ada using : `ssh s-ada`. <br>
The dip environment has already been created. <br>
Find the project under
`/home/shaunak/sem7/DIP/project-adobe-literoom`. <br>
Activate the conda environment and setup port forwarding as explained in method 1.


## Images : 

* Find the images used in the assignment [here](https://drive.google.com/drive/folders/1zVqD-mrVhgGheZyROJRnEC3KsVDw3eFv?usp=sharing).

* Make sure to edit the `IMAGES_PATH` variable in the notebook after downloading. Do not download in this folder or any subdirectory in this folder.
