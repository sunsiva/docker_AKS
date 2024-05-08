# when this dockerfile is requested to executed use the dcoker build command
# dcoker allocates a process called intermedicate container to perform the build

#pull the server image
FROM mcr.microsoft.com/windows/servercore:ltsc2022
# copy myscript.psq into c; as yourscript.ps1
COPY scripts/myscript.ps1 c:\\yourscript.ps1

# set the startup command when the container is called to run
CMD [ "powershell","c:\\yourscript.ps1" ]