# escape=`
FROM minecraft-server:nanoserver

SHELL ["powershell", "-Command", "$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]

ENV EULA=TRUE `
    ONLINE_MODE=FALSE `
    SEED=-9363708386013540 `
    VERSION=1.12.1 `
    DIFFICULTY=peaceful `
    GUI=FALSE `
    CONSOLE=FALSE

# RUN net use F: \\minecraftworld.file.core.windows.net\mcworld1  /u:AZURE\minecraftworld ZuZsaL2zOLuqKGqZFCyX3XRLeP0Y7mjAvzEtTy3dLNtF9mSeTsAeLkAhGU09Y3vmDOc0a/IwNFE+ZUkpq7iLpw==


# RUN $minecraft = Start-Process -FilePath 'powershell' -Args @('-File C:\minecraft\start.ps1') -RedirectStandardOutput minecraft.out -PassThru; `
#     Start-Sleep -Seconds 2; `
#     while((Select-String -Pattern 'RCON running' -Path G:\minecraft.out) -eq $null) { Start-Sleep -Seconds 1 }; `
#     rcon-cli --host 127.0.0.1 --port 25575 --password minecraft setworldspawn 555 66 439; `
#     rcon-cli --host 127.0.0.1 --port 25575 --password minecraft gamerule doDaylightCycle false; `
#     rcon-cli --host 127.0.0.1 --port 25575 --password minecraft time set 6000; `
#     rcon-cli --host 127.0.0.1 --port 25575 --password minecraft stop; ` 
#     Wait-Process -InputObject $minecraft; `
#     rm eula.txt; `
#     rm minecraft.out; `
#     rm server.properties; `
#     rm -r ./logs; 

ENV EULA=TRUE`
    RCON_PASSWORD=cheesesteakjimmys

COPY customstart.ps1 C:\minecraft

WORKDIR c:\

ENTRYPOINT [ "powershell", "-File", "C:\\minecraft\\customstart.ps1" ]