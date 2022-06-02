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

# Screenshot



# Instructions to Run
> Please note the Following instructions are for a linux distro.
> Instructions on other operating system might vary.

**Prerequisites:**

Requires `docker` and `docker-componse` to be installed on your machine.


1. git clone ns-ceiling-fan monorepo
```bash
git clone https://github.com/dinbtechit/ns-ceiling-fan.git
```
2. git pull all submodules
```
git pull --recurse-submodules
```
3. Build Images and bring up the application.
```
http://192.168.195.128:3000/api/v1/fan/status
```
**output:**
```
...
Successfully built 2e19b15cdbd8
Successfully tagged ns-ceiling-fan_frontend:latest
Creating frontend ... done
Creating redis    ... done
Creating backend  ... done

```

4. Open browser preferably chrome (NSFan is not supported on IE)

> **Note:** website is accessible only on localhost.
```
http://localhost:8080
```

5. NSFan Demo

![](/u1/code/personal/novascotia/ns-ceiling-fan/readme/demo.gif)
