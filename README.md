```shell
sudo add-apt-repository ppa:deadsnakes/ppa

export UID=$(id -u)
export GID=$(id -g)

docker run --rm -it \
   --user $UID:$GID \
   -v /etc/group:/etc/group:ro \
   -v /etc/passwd:/etc/passwd:ro \
   -v /etc/shadow:/etc/shadow:ro \
   -v ~/:/home/$USER \
   --workdir="/home/$USER/dev/tercen/mkdoc_playground" \
   python:bullseye bash


pip3 install -r script/requirements_docs.txt

PATH=/home/alex/.local/bin:$PATH

export GIT_COMMITTER_NAME=ci-bot
export GIT_COMMITTER_EMAIL=ci-bot@tercen.com

mike delete --all
mike deploy --push --branch gh-pages 1.0

mike deploy --remote origin --push --branch gh-pages

pip install mkdocs
pip install mike


mkdocs new documentation

cd documentation
mkdocs serve
mkdocs build

echo "site/" >> .gitignore


python3 -m http.server
```