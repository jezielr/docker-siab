## Docker Shell in a box
https://hub.docker.com/r/sspreitzer/shellinabox

Colocar IP al host a conectar y asignar identificador que no exista ya que este crea ese usuario

´´´
docker run -d --name siab -p 4200:4200 \
  -e SIAB_USERID=1001 \
  -e SIAB_GROUPID=1001 \
  -e SIAB_SERVICE="/:SSH:192.168.31.155" \
  -e SIAB_SSL=false \
  --restart unless-stopped \
  sspreitzer/shellinabox:latest
´´´

Especialmente para navegadores antiguos que no soporte JavaScript en su totalidad
