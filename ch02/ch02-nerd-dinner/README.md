[Weekly Windows Dockerfile #12](https://blog.sixeyed.com/windows-weekly-dockerfile-12-nerddinner/)

# Notas de entendimento

Diferente do conceito tradicional de uma aplicação APS.NET, no docker devemos rodar uma aplicação por caontainer. Por isso é mantido apenas um application pool por aplicação. Os demais sites e appplication pool são removidos.

# Destravar o web.config
Por padrão o IIS trava o acesso ao web.config. Não entendi ainda a razão. Para destravar, no exemplo do nerd-dinner, usa-se a instrução abaixo no:

´´´
RUN & c:\windows\system32\inetsrv\appcmd.exe `
      unlock config `
      /section:system.webServer/handlers
´´´

