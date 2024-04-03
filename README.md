# denv
A simple dockerized development environment.

I fart around, poking at random projects in a variety of languages quite a bit.
Mostly to learn new things and satisfy curiosity. Rather than installing the
tools, libraries, dependencies, etc on my local machine I like to keep them in
docker containers so I can easily throw it away later.

This also makes rebuilding my laptop (something I do quite often as well) easy
because I don't need to remember what to put back: the laptop remains largely
bare-bones.

This image is just a base that contains some stuff I tend to use everywhere:
curl, wget, git, etc.

It also includes nvim configs and other local settings that most normal folk
would include in their home directory somewhere.

# Usage
You'll need `make` and `docker` installed, but that's about it.

1. Run `make docker` to build the image itself. Later, you can run `make dev`
   to bash into it interactively.
2. Create a docker file in other project that uses the one above and adds their
   own stuff to create a project-specific build/dev environment.
3. Copy the makefile over to your project and fiddle with the project name so
   it'll build the right things.
