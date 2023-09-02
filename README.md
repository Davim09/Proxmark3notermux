# Proxmark3 no termux
Funcionando em um proxmark3 já com firmware, esse método esta funcionando apenas como um modo portátil "standalone" com terminal.

# Instalando Requerimentos:
```
pkg updade
```
```
pkg upgrade
```
```
pkg install make clang readline libc++ git binutils
```
```
git clone https://github.com/RfidResearchGroup/proxmark3.git
```
```
cd proxmark3
```
```
make clean && make client
```
# Abrindo o terminal do proxmark3 no Temux
Conecte o proxmark3 no celular com cabo otg

Instale o aplicativo TCPUART
Dentro dele em cima onde tem USB_UART clique em connect ele irá pedir permissão para que o acesse o proxmark3
Logo em baixo, onde tem TCP (server stopped), Marque a caixinha server e colocar porta 8080, e clique em start

<img loading="lazy" src="https://raw.githubusercontent.com/Davim09/Proxmark3notermux/main/Screenshot_2023-09-02-12-20-18-062_com.hardcodedjoy.tcpuart.jpg" width="419" height="927"/>

Voltando para o termux, verifique se está dentro da pasta proxmark3, para isso digite:
```
ls
```
Se aparecer um várias de pastas incluindo a pasta client então vc está dentro da pasta do proxmark3, se não aparecer as pastas, digite o comando:
```
cd proxmark3
```
Após dentro lá pasta client vc irá digitar esse comando:
```
./client/proxmark3 tcp:localhost:8080
```
Assim ele irá abrir o terminal do proxmark3, lembrando que se vc desconectar ele do USB tera que ir lá no aplicativo TCPUART e fazer ele conectar novamente na primeira opção.

Para mais informações:
https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/termux_notes.md
