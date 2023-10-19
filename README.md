# archyo
An Arch Linux Based Docker Image. 

**Author**: *Rene Pineda*.

GNU GPL v3.

#### Default configuration:
* A default sudo user named **archyo**
  * The user can be overriden during the build via **--build-arg yo_user=<your_user>**
* Default installed apps:
  * sudo 
  * openssh
  * vim
  * Additional apps can be specified via **--build-arg yo_apps='a b c'**
 * ssh sever will listen on port 22
 
 #### Image customization example:

```
docker build \
  --build-arg yo_user=neo_matrix4 \
  --build-arg yo_apps='jdk11-openjdk maven sshpass git unzip jq yq nodejs github-cli' \
  -t archyo \
  -f Dockerfile-archyo \
  /some/working/dir
