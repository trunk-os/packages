include ../include.mk

run: down
	sudo podman run -it -d --privileged --name "$(NAME)" --net bridge --pid host -v /etc/systemd:/etc/systemd:shared -v /trunk:/trunk:shared "$(LATEST_TAG)"
