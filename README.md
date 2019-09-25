# Description
Simple docker image containing Meson, Ninja, Vala compiler and GTK libraries
that allows you to build Vala projects using meson.

# Building a Vala project in the current folder

````
docker run --rm -v $PWD:/build \
    uploadedlobster/meson-valac \
    /bin/sh -c "cd /build; meson builddir; cd builddir; ninja test"
````

# Using with Travis CI
For a full example how this image can be used for a Travis CI build see
https://github.com/phw/peek/blob/master/.travis.yml
