# projeto-ponto-eletronico
engenharia reversa do firmware de um ponto eletronico com biometria

O objetivo deste projeto é realizar uma engenharia reversa de um ponto biometrico.
descricao do firmware:
modelo: KB-007
Release Date: 2014-09-03
Serial No.: 20140925557
Firmware: WS306BV6 v2.01
USB Model Parameter: 39322200

descricao do hardware:
SRDAM: ESMT M12L64164A
micocontrolador / microprocessador: desconhecido ate o momento
flash: WINBOND W25Q32FV
a placa possui pinos de conexao UART, LAN-485, USB e mini USB.
incrições na placa:
  - AST6801WFS_V1.4
  - 2014.2.19.JKC

foi realizado o dump da memoria flash utilizando uma gravadora / leitora de EPROM CH341a com o seguinte comando no terminal do ubuntu 24.04.3 LTS:
- sudo flashrom -p ch341a_spi -r backup.rom

apos o dump foi realizado uma extracao do arquivo .rom usando o seguite comando:
- binwalk --dd=".*" backup.rom

neste momento os arquivos binarios extraidos estado sendo analisados.
