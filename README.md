# yoshimi.github.io

Markup, style data and media for the yoshimi website,
along with a simple site generation script.

## Building

Python 2.7+ (or 3.5+) is required to generate the site.

Run `./gen_site` in the _site directory to generate the site.
The resulting files will be placed in a directory called 'out'

If you want to write the output somewhere else, you can use the `BUILD_DIR`
environment variable, for example like this:
```
BUILD_DIR=/home/me/www/my_audio_websites/yoshimi/ ./gen_site
```
or
```
export BUILD_DIR=/home/me/www/my_audio_websites/yoshimi/
./gen_site
```
or
```
BUILD_DIR=.. ./gen_site
```

## Committing/Deploying

When making changes, make sure that you are editing the sources under
the _site directory. When you want to deploy the changes, run the
`./gen_site.py` script as shown above.

* If you have only modified existing files, run `git add -u` and commit.

* If you have added new files in _site, you must also add the corresponding
deployed files under root before committing.

* If you have removed or renamed files in _site, you must perform the
corresponding operations on the files' deployed counterparts .

> *Yes, this is clearly awful, and should be fixed by either moving to Jekyll*
> *or by creating some other separation between sources and output files.*
