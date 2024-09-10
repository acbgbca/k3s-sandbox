# k3s Sandbox

This is designed as a throw away environment that can be used for learning and experimenting with k3s. It runs a single node k3s cluster within docker, with supporting containers to help test the services that are running.

Note: The dev container will only work if you check the code out on your computer and then reopen in the dev container. It will not work when checked out in a volume, or via Codespaces. This is due to the need to mount the dnsmasq config file into the container.