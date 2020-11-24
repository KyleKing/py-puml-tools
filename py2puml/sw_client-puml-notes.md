Generate the text UML (in `cd ./py2puml/`)

```sh
PKG=sw_client

poetry run ./py2puml.py --config $PKG.ini --root $ROOT -o $ROOT/py2puml-$PKG.puml $ROOT/$PKG/api_client.py $ROOT/$PKG/borg.py $ROOT/$PKG/command_line_app.py $ROOT/$PKG/command_sets.py $ROOT/$PKG/user.py $ROOT/$PKG/utils_argparse.py
```

Then output PNG and SVG images

```sh
cd $ROOT/_diagrams
plantuml $PKG.puml
plantuml $PKG.puml -tsvg
```
