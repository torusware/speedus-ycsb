![speedus logo](http://dl.torusware.com/images/speedus_small.jpg "Torusware Speedus")

# Speedus Plug&Run Lite for YCSB
Ubuntu image with Yahoo! Cloud Serving Benchmark (YCSB) and speedus solution for high-performance communications. Check us out at [our website](http://torusware.com/).

Speedus is your communications highway:

- Accelerates communications in the cloud and corporate IT systems
- Faster applications provide businesses with higher competitive advantages while reducing their IT bill
- 100% nonintrusive software solution which takes full advantage of the underlying hardware

# Supported tags and respective `Dockerfile` link
Each tag corresponds to the tag of the ubuntu base image:

- [`2.0`](https://github.com/torusware/speedus-ycsb/tree/master/2.0 "2.0 Dockerfile"), [`latest`](https://github.com/torusware/speedus-ycsb/tree/master/2.0 "latest Dockerfile")

# Launching instructions
In order to run a container with our image, execute:

    sudo docker run -ti torusware/speedus-ycsb

This will launch a `bash` shell where you can execute whatever program you want.

The YCSB is installed on the home folder and added to the path, so just type:

    ycsb -h

And it will show you the help menu of the ycsb. In order to run it with speedus, type:

    speedus ycsb -h

In this image we provide a built-in communication tests as well, Netpipe. Just execute:

    NPtcp &
    NPtcp -h localhost

For getting the baseline. To perform the test with our solution:

    speedus NPtcp &
    speedus NPtcp -h localhost

As you can see, using speedus is really easy and non-intrusive, just type `speedus` before your application:

    speedus /path/to/the/program [parameters]

If you need more information, you can check the README file inside the container or contact us at <info@torusware.com>
