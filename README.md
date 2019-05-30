# LibreOffice headless mode Docker image

Running headless libreoffice can help for various use cases. For example converting office documents with a better result than unoconv does.

# Build

[![Docker Repository on Quay](https://quay.io/repository/khalibre/libreoffice-headless/status "Docker Repository on Quay")](https://quay.io/repository/khalibre/libreoffice-headless)

# Port available

The native port is exposed:

    8100

External volumes

This volume is declared:

    /usr/local/share/fonts/: to mount your fonts folder.

Environment variables

Even if the default values are the most suggested, if necessary, it's possible to customize their behavior through these variables:

    HOST_IN: the hostname or IP of the external client accepted as input.
        default: 0 (any external hosts)
    PORT_IN: the listening port used by external clients to connect to the container.
        default: 8100
    LANG: it enables the UTF-8 locale coding in the internal filesystem of the container.
        default: C.UTF-8 (highly suggested)
