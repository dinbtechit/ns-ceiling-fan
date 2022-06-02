# NS Ceiling Fan

## Frontend
A front-end to interact with the fan and the display its status and settings.
> Ideally use these Government of Nova Scotia UI frameworks
Forms & Services Building Blocks
Pattern Library

## Backend
A back-end to handle the logic for operating the fan as follows:
- The fan has two pull cords:
- One to increase the speed each time it is pulled.
0, 1, 2, 3 speeds
- If pulled on speed 3, returns to 0 (“off”)
- One to reverse direction at the current speed setting
- Remain in same direction as speeds are cycled, until reversed again


# Instructions to Run
> Please note the Following instructions are for a linux distro.
> Instructions on other operating system might vary.

### Prerequisites:

Requires following to be installed on the machine.
1. git (latest)
2. docker - version 20.10.16 or higher
3. docker-compose - version 1.29.2 or higher

### Steps

1. git clone ns-ceiling-fan monorepo
```bash
git clone https://github.com/dinbtechit/ns-ceiling-fan.git
```
2. cd into the cloned repo
```bash
cd ns-ceiling-fan
```
3. git pull all submodules
```bash
git submodule init
git pull --recurse-submodules  && git submodule update --recursive
git submodule update --remote --merge
```
4. Build Images and bring up the application.
```bash
docker-compose up -d --build frontend backend
```
**output:**
```
Successfully built 2e19b15cdbd8
Successfully tagged ns-ceiling-fan_frontend:latest
Creating frontend ... done
Creating redis    ... done
Creating backend  ... done
```

5. Open browser preferably chrome (NSFan is not supported on IE)

> **Note:** website is accessible only on localhost.
```
http://localhost:8080
```

6. NSFan Demo

<p align="center">
 <img src="https://user-images.githubusercontent.com/17984781/171552948-8104601a-1563-4952-9ce8-852e07f2d402.gif"/>
</p>


7. To stop all the containers & clean all the docker files
```
$ docker-compose down
$ docker system prune -f
$ docker image prune -f
$ docker container prune -f
$ docker volume prune -f
```
**output**
```                          
Stopping frontend ... done
Stopping backend  ... done
Stopping redis    ... done
Removing frontend ... done
Removing backend  ... done
Removing redis    ... done
Removing network ns-ceiling-fan_default
```

# Thank you
