# Ember - search for unused components

Very dummy code snippet to search for all components in Ember app that are not used anymore

```python
# Run in python
import glob, os

jsComponents = [line.strip().replace("app/components/", "").replace("/component.js", "") for line in glob.glob("app/components/*/*.js")]
hbsComponents = [line.strip().replace("app/components/", "").replace("/template.hbs", "") for line in glob.glob("app/components/*/*.hbs")]
components = list(set(jsComponents + hbsComponents))

files = glob.glob("app/**/*.*", recursive=True)

for component in components:
  used = False
  for file in files:
    if component in open(file).read():
      used = True

  if not used:
    print(component + ", " + str(used))
```

