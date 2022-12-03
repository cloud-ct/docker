# syntax=docker/dockerfile:1
  FROM mcr.microsoft.com/dotnet/aspnet:5.0-focal AS runtime

  RUN apt-get update -qq
  
  RUN apt-get -y upgrade
  RUN apt-get -y install gnupg2 wget vim
  RUN apt-cache search postgresql | grep postgresql
  RUN sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt focal-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

  RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -

  RUN apt-get update -qq

  RUN apt-get -y install postgresql-10
  RUN apt-get -y install postgresql-13
