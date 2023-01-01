# About this documentation

This documentation is still in its early stages.

## How to contribute

In order to contribute to the documentation, one has to follow the following steps :

- Install MkDocs and the Material theme
```bash
root@dfly# pkg install py39-mkdocs py39-mkdocs-material
```

- Fork the [git repository](https://github.com/DragonFlyBSD/docs.dragonflybsd.org) and clone your fork
```bash
user@dfly% git clone https://github.com/yourgithubuser/docs.dragonflybsd.org
user@dfly% cd docs.dragonflybsd.org

```

- Build the website (check mkdocs build -h for more options about the building phase)
```bash
user@dfly% mkdocs build
INFO     -  Cleaning site directory
INFO     -  Building documentation to directory: /home/youruser/docs.dragonflybsd.org/site
INFO     -  Documentation built in 1.08 seconds 
```

- (*Optional step*) Serve the website with MkDocs embedded server to 
```bash
user@dfly% mkdocs serve
INFO     -  Building documentation...
INFO     -  Cleaning site directory
INFO     -  Documentation built in 1.06 seconds
INFO     -  [18:25:58] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO     -  [18:25:58] Serving on http://127.0.0.1:8000/
INFO     -  [18:25:59] Browser connected: http://127.0.0.1/
```

- Modify some content and rebuild the website (at least before commiting)
```bash
# This is an example of how this page was created
user@dfly% git checkout -b contribution # the git branch contribution is created
add the desired content in docs/about.md
user@dfly% mkdocs build # then review the website or live-preview it if using the serve option
user@dfly% git add docs/about.md
user@dfly% git commit -m "Add contribution instructions"
user@dfly% git push origin contribution # we push to the remote contribution branch
```

- Open a pull-request on the [Github page](https://github.com/DragonFlyBSD/docs.dragonflybsd.org/pulls)
