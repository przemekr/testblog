---
layout: post
title: And what about the code?
date: 2015-06-19 12:28:02
---

This should come as a code snipped, with syntax highliting:

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}


{% highlight bash linenos %}
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
{% endhighlight %}
