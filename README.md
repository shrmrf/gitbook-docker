# gitbook-docker

[GitBook](https://github.com/GitbookIO/gitbook) installed in a Docker container.

This image can be used to build books with the GitBook CLI.

> NOTE: The image is created with the current version of GitBook installed at the time the image was created. You can add a different version, but beware that by default the GitBook CLI installs GitBook versions in $HOME (i.e. `/root` with the current configuration), which will disappear when the container is shutdown unless you map it to a local directory.


## Usage

### Use Case #1: Generating HTML

To run gitbook with the current directory mounted to `/docs`:

    $ docker run -ti --rm -v `pwd`:/docs shrmrf/gitbook-docker <path to your book>


### Use Case #2: Building a PDF

    $ docker run -ti --rm -v `pwd`:/docs shrmrf/gitbook-docker pdf <path to your book>

### Acknowledgements
This is just a blatant fork off of humangeo/gitbook-docker. Thanks humangeo :)
