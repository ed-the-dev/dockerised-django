Steps:

Write a docker file and a docker compose.

Then, I can't use the compose command to mount to the container if there's no on-going process, as the container without that will finish immediately.

So I have to write my own command (annoying) mounting the volume.

`docker images` to list images... 

Then:

(I need to add bash on, because for this base image it starts you with the Python console)

`docker run -it -v $(pwd):/code django-docker-example-app bash`

This keeps the container open, I can then install anything I want into the code folder as I'm using volumes.

From here I should be able to pip install django (done - set up a venv next time), and then create a Django project without ever installing Django or the latest version of Python on my machine. (done).

Now, consider my docker-compose, the container won't immediately stop if I'm running the Django server.
