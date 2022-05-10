#programowanie #HTML #CSS 

In the previous lecture, we started a **local development web server** via the "Live Server" Extension for VS Code.

#### What Is A "Development Web Server"?

It's a "local development web server" because it's a web server software that serves the website locally, on our machine. It's **NOT exposing** our machine or the website to the internet - you can only visit and reach it locally (i.e. from your machine).

This "web server software" (i.e. the "Live Server" extension in this case) is a software that does actually listen for incoming HTTP requests and send back appropriate responses (that contain the HTML code for example). Remember that **request + response** image form the first course section!

_Later in the course, we'll also set up our own web server that is able to do more things than just send back pre-defined HTML code. We'll dive into the creation of our own backend and our own web server with a technology called "NodeJS" from section 16 on._

#### What's This Address: 127.0.0.1?

As mentioned above, this development web server **hosts** (= provides / serves) the website **from our local machine to our local machine**.

In section 1, you learned that users enter addresses (URLs) into the browser address bar to reach a website and send such a request. You also learned that the human-readable "domains" (like academind.com) are translated to IP addresses which act as unique identifiers of machines connected to the internet.

`**127.0.0.1**` **is such an IP - though it's a special one!**

`127.0.0.1` is a special IP, that's **reserved to your local machine**. And it's the **local machine for everyone**!

If I type `127.0.0.1` into the browser, I connect to **my** local machine (if it's running a local web server). You reach **your** machine.

It's an IP address that's NOT assigned to other machines in the world wide web - instead it's reserved as a "placeholder" that always points at your local machine. It exists for use-cases as we have it here: For development on our local machine, where we want to test our website with help of a local development server. I.e. we can test it locally without exposing it to the entire world yet.

There also is an **alias** (basically like a "special domain name") that you can use locally, instead of `127.0.0.1`: `localhost`. You can also enter `localhost` into your browser and it will be the same as if you entered `127.0.0.1`. So `localhost:5500` is a replacement for `127.0.0.1`.

#### What's This Thing: :5500?

The `:5500` part is a so-called "**port**".

Ports are another concept from the networking world. The idea is, that a machine can **expose different processes** (e.g. different web servers serving different websites) via different ports.

So a single machine could host / provide three different websites on three different ports. The IP address of the local machine would always be the same (`127.0.0.1`) but every website would have its own port (e.g. `5500`, `3000`, `8080`).

If you move a website to some machine that IS exposed to the world wide web (i.e. you publish it, you don't run it via a development web server on your local machine anymore), then the website is reached via the IP address of that remote machine. Or, typically, via a domain that's pointing at that IP address.

In addition, this port concept also still exists: When exposed to the world wide web, websites are typically served on ports `80` (HTTP) or `443` (HTTPS). You don't need to worry about this right now though. When publishing a website (covered later in the course), the different hosting providers typically take care about exposing the right ports automatically.

When working on your local machine, you don't use these "common ports" (`80`, `443`) since you're not exposing the website to the world wide web anyways. Instead, you can use **ANY ports that are typically not used by any other processes** - `5500`, `3000` or `8080` are common choices because they aren't typically used by other processes.

That's why the "Live Server" extension does use port `5500` for serving your website locally.

And you target a specific port by adding `:<port-number>` after the domain or IP address. That's why `127.0.0.1:5500` resolves to that locally served website. Alternatively, since `127.0.0.1` is aliased with `localhost`, you could also enter `localhost:5500`.

You can try this with other websites, too!

Try visiting `academind.com:443` or `academind.com:80` => You will see the regular Academind website. Of course you don't need to add the extra port information in the URL though - since `80` and `443` are the defaults, the browser will use these ports automatically, if you enter a website address.