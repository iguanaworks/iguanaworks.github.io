# On December 31st, 2025 Iguanaworks closed down. 

It was a fun 20 years.

## Source Code

Our software is available on our [github repository](https://github.com/iguanaworks). The source code for igclient and igdaemon to control the Iguanaworks USB IR Transceiver is at [here](https://github.com/iguanaworks/iguanair) and the source for the LIRC driver is [here](https://github.com/iguanaworks/iguanair-lirc).

## Binary Files

We no longer maintain any builds or binary files. For Ubuntu / Debian, our ppa is not updated, but it has binaries for old distro's that may still work. You can try with

```
sudo add-apt-repository ppa:iguanaworks/iguanair
sudo apt-get update
```

The ppa is avialable [here](https://launchpad.net/~iguanaworks/+archive/ubuntu/iguanair).

For Redhat / Fedora / RPM based distros, our repository is no longer available. You can directly download our latest binary builds [here](https://github.com/iguanaworks/website-backup/tree/main/Binaries).

For Windows, our latest binaries are also availabe [here](https://github.com/iguanaworks/website-backup/tree/main/Binaries).

## Documentation

A very basic conversion of our WordPress website to markdown is available [here](https://github.com/iguanaworks/website-backup) and has some basic information about our hardware (see [usb_ir_transceiver.md](https://github.com/iguanaworks/website-backup/blob/main/products/usb-ir-transceiver.md) for example.

Additionally, our very out-dated wiki is no longer available, its content has a git backend and is available [here](https://github.com/iguanaworks/Wiki).

## Testing

List of files:

<ul>
  {% for page in site.pages %}
    {% if page.title %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
