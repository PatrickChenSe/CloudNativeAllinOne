## Bash writing skill

### templates
I found this template on [line](https://gist.github.com/m-radzikowski/53e0b39e9a59a1518990e76c2bff8038).And copy/paste it here in my code repository. This is simple and concise template including several important points of writing bash shell.

* Safe & Security. Exit when there is an error, and clean up with trap function.
* Param parsing and help usage message. This is most a must have for every decent bash script. And I always forgot about how to parse param in bash, always need to google it. 
```bash
while :; do
  case "${1-}" in
  -h | --help) usage ;;
  -p | --param) 
    param="${2-}"
    shift # delete current
  -?*) die "Unknow option: $1" ;;
  *) break ;;
  esec
  shift
done

```
* Exit func, wrap error msg output and exit with code in a func is good practice.
```
echo >&2 -e "${1-}"
```
* setup_colors is something I don't know before. Good to learn.

### other resources
more templates: https://github.com/ralish/bash-script-template
CLI guidelines: https://clig.dev/

