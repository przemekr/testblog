---
layout: post
title: And what about the code?
date: 2015-06-19 12:28:02
---

This should come as a code snipped, with syntax highliting:

```javascript
hendleHeader()
{
    k=$1
    v=$2
    echo $k $v >> log
    case $k in
       Subject)
          hendleSubject $v
          ;;
       *)
          ;;
    esac
}
while IFS= read -r LINE; do
    echo "$LINE" >> mail
    case $LINE in
       "")
          hendleContent;;
       *)
          key=$(echo $LINE | cut -d: -f1)
          value=$(echo $LINE | cut -d: -f2-)
          echo "key: $key" >> log
          echo "value: $value" >> log
          hendleHeader $key "$value"
          ;;
    esac
done
exit 0
```


```
function test() {
  console.log("notice the blank line before this function?");
}
```


Code blocks can be taken a step further by adding syntax highlighting. In your
fenced block, add an optional language identifier and we'll run it through
syntax highlighting. For example, to syntax highlight Ruby code:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```



