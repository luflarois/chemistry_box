# chemistry BRAMS - BOX
##Um pacote de teste para o solver - Migração para IA

### Para compilar

entre no diretório build e dê o comando make
ele vai criar o chem.x que é o executável.

### Para rodar:

Tendo rodado o BRAMS modificado (branch chem_ia) e obtido os arquivos de entrada:

chem_inp_tttttt_pppp.bin
onde:

tttttt - é o tempo da rodada
pppp - é o processador que gerou a saída

Preencha o namelist target.nml com a seguinte informação:

```
&target
time = 30.0,
processor = 1,
&end
```

Onde informa qual arquivo será lido, no caso acima tempo 30 seg e processador 1.

APós isso, rode o chem.x que ele vai rodar e gerar a saída de nome:

chem_std_tttttt_pppp.bin

Que pode ser comparada com:

chem_out_tttttt_pppp.bin (gerada pelo modelo).

