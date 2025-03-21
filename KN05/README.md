# KN05: Arbeit mit Speicher

## Bind mounts

Docker Startbefehl: `docker run -it -v /mnt/c/Users/matth/Documents/School/M347_TBZ/KN05/scripts:/home nginx:latest`

<video controls src="KN05A.mp4" title="KN05-A"></video>

## Volumes

Docker Startbefehle:
`docker run -itd --mount type=volume,src=KN05B,dst=/home --name KN05B-1 nginx:latest`
`docker run -itd --mount type=volume,src=KN05B,dst=/home --name KN05B-2 nginx:latest`

<video controls src="KN05B.mp4" title="KN05-B"></video>

## Speicher mit docker compose

![KN05-Frontend](<Screenshot 2025-03-21 100619.png>)

![KN05-Backend](<Screenshot 2025-03-21 100400.png>)