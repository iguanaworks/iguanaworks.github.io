# On December 31st, 2025 Iguanaworks closed down. 

It was a fun 20 years.


## Documentation

A very basic conversion of your WordPress website was converting to markdown and the product pages can be viewed here:

<ul>
  {% for page in site.pages %}
    {% if page.path contains 'products/' %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

## Source Code

Our software is available on our [github repository](https://github.com/iguanaworks). The source code for igclient and igdaemon to control the Iguanaworks USB IR Transceiver is at [here](https://github.com/iguanaworks/iguanair) and the source for the LIRC driver is [here](https://github.com/iguanaworks/iguanair-lirc).


Additionally, our very out-dated wiki is no longer available, its content has a git backend and is available [here](https://github.com/iguanaworks/Wiki).

## Binary Files

We no longer maintain any builds or binary files. For Ubuntu / Debian, our ppa is not updated, but it has binaries for old distro's that may still work. You can try with

```
sudo add-apt-repository ppa:iguanaworks/iguanair
sudo apt-get update
```

The ppa is avialable [here](https://launchpad.net/~iguanaworks/+archive/ubuntu/iguanair).

For all other OS's and distros, our latest binary files are available here:


<ul>
  {% for file in site.static_files %}
    {% if file.path contains '/Binaries' %}
      <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

