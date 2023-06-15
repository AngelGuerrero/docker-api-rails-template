# Imagen base para Ruby on Rails 6
FROM ruby:3.0.0

# Instalar dependencias del sistema
RUN apt-get update -qq && apt-get install -y postgresql-client

# Configurar directorio de trabajo en el contenedor
WORKDIR /api

# Copiar el Gemfile y el Gemfile.lock al contenedor
COPY Gemfile Gemfile.lock Procfile /api/

RUN mkdir -p /api/log && touch /api/log/development.log

# Instalar las gemas
RUN gem install bundler
RUN bundle install

# Copiar el resto de la aplicación al contenedor
COPY . /api

RUN gem install foreman

EXPOSE 3000