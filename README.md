![Logo](https://cloud.githubusercontent.com/assets/4998038/8658729/8b3a918c-299d-11e5-8452-6b1b22c51618.png)

[![License](https://poser.pugx.org/alorel/alo-cookie/license?format=plastic)](LICENSE)


# What is this sorcery ? #
It's a simple class to manipulate cookies in an object-oriented manner.

# Usage #

## Get all document cookies ##

    var cookies = AloCookie.getAll();
    // {name1:value1, name2:value2 ...}

## Setting cookie "foo" ##

    var cookie = new AloCookie("foo");
    cookie.value = "bar";
    cookie.expire = 3600; //in 1 hour. Defaults to expire at the end of the session
    cookie.domain = "www.example.com"; //defaults to window.location.hostname
    cookie.path = "/cart/checkout"; // Defaults to "/"
    cookie.secure = true; // true sends the cookie only via HTTPS. Defaults to window.location.protocol == "https:"
    cookie.save()


## Check if cookie called "foo" exists ##

    var cookie = new AloCookie("foo"),
    cookieExists = cookie.exists();

## Deleting cookie "foo" ##

    var cookie = new AloCookie("foo");
    cookie.remove();
