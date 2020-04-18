# Alarme-coronavirus
Programa para alarme de coronavirus com a biblioteca XT_DAC_Audio e esp32

Passo a passo:
Tutorial 1:
https://www.youtube.com/watch?v=gxpHDUHcBMk

Download da Biblioteca usada:
 Versão: XT_DAC_Audio 4_2_1  
 https://www.xtronical.com/the-dacaudio-library-download-and-installation/
 
IDE arduino:
Após download da biblioteca, clicar em sketch -> adicionar biblioteca zip, selecionar o arquivo zip da biblioteca. Após instalar, reiniciar a ide do arduino. 
Ao reiniciar, cicar em arquivo -> exemplos -> XT_DAC_Audio -> Playwav

Música utilizada:
  Música astronomia versão https://youtu.be/VlLkvvRCSWk
  

Edição da música no audacity:
  Site para download: https://www.audacityteam.org/
  Importar a música
  Colocar mudar Taxa do projeto para 8000 (Hz)
  Ir em Faixa/mixar/mixar e processar
  Ir em arquivo/exportar/exportar áudio como wave 
  Nomear e selecionar tipo "outros arquivos sem compactação" e codificação "unsigned 8-bit PCM" e salvar

Código da música:
  No programa HxD Hex Editor(https://mh-nexus.de/en/hxd/), clicar em arquivo-> abrir-> selecionar arquivo wave editado;
  Selecionar Tudo(ctrl+A), clicar em editar ->  copiar como-> C
  Na ide, na aba SoundData.h, colar o arquivo e adicionar a palavra-chave "PROGMEM" após unsigned char e altere se quiser o nome do vetor de dados(ex:  rawdata[] -> astronomia[]. Ficaria: "unsigned char PROGMEM astronomia[]".
  Na aba principal(Alarme_coronavirus), no objeto Alarme da classe XT_Wav_Class, colocar como parâmetro nome aderido no vetor de dados, no caso "astronomia". Ficando assim: XT_Wav_Class Alarme(astronomia);
  
  Links adicionais para mais informações a respeito de DAC do esp32:
   
   Tech Note 071 - ESP32 Digital to Analogue Converter
   https://www.youtube.com/watch?v=T4jg1j0XgWU
   
   ESP32: Você sabe o que é DAC?
   https://www.youtube.com/watch?v=Rg-0Jq8TOEw
  

, 
