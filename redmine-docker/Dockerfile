# Baseado na imagem oficial do Redmine
FROM redmine:latest

# Define o diretório de trabalho
WORKDIR /usr/src/redmine

# Cria o tema diretamente no Dockerfile
RUN mkdir -p public/themes/meu_tema_simples/stylesheets && \
    mkdir -p public/themes/meu_tema_simples/images && \
    echo "/* Meu Tema Simples */" > public/themes/meu_tema_simples/stylesheets/application.css && \
    echo "body { font-family: Arial, sans-serif; background-color:rgb(49, 31, 31); color: #333; }" >> public/themes/meu_tema_simples/stylesheets/application.css


RUN chown -R redmine:redmine public/themes && \
    chmod -R 755 public/themes


# Exposição da porta padrão do Redmine
EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]
