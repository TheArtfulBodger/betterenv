# Better ENV

A wrapper around `os.environ` to add some features inspired by linuxserver.io docker images.

## Usage

```py

import betterenv as env

# get an environmental variable
env.get("CONF_FILE")
env.get("CONF_FILE", "default_value")


# gets a list of environmental variables
env.keys()

# get structured keys
env.structured_keys("BETTERENV")
```

## Structured Keys
Designed as an override for configparser, if you have the following output 
```bash
export BETTERENV__section__key=value
```
```json
{
  "section":{
    "key":"value"
   }
}
```