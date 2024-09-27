# Formatting SD (Mac)

## Required Reading

Essa é uma seção adicional para a formatação de um cartão SD para fazê-lo funcional com o 3DS.

Se o 3DS já reconhece o cartão SD, este guia não é necessário.

Esta página é destinada apenas a usuários do Mac. Caso você não esteja usando Mac, acesse a página [Formatando SD (Windows)](formatting-sd-\(Windows\)) ou [Formatting SD (Linux)](formatting-sd-\(linux\)).

## Instructions

### OS X El Capitan (10.11) and later

1. Insira o cartão SD no seu computador

2. Se o cartão SD tiver quaisquer arquivos ou pastas nele, copie tudo para uma pasta no seu computador

3. Execute o aplicativo Disk Utility

4. No menu "View" no canto superior esquerdo, escolha "Show All Devices"

5. Selecione seu cartão SD no painel da esquerda

   ::: danger

   Certifique-se de escolher o dispositivo correto, caso contrário você pode apagar a unidade errada acidentalmente!

   :::

6. Clique em "Erase" no topo

7. Digite qualquer coisa no campo "Name"

8. Certifique-se de que "Format" está definido como "MS-DOS (FAT)"

9. Certifique-se de que o "Scheme" está definido como "Master Boot Record"
   - If "Scheme" does not appear, click "Cancel" and make sure to choose the device instead of a volume

10. Clique em "Erase"

11. Aguarde a conclusão da formatação

12. Clique em "Close"

13. Se o cartão SD tinha quaisquer arquivos ou pastas nele, copie tudo de volta para o SD do seu computador

### OS X Yosemite (10.10) and earlier

1. Insira o cartão SD no seu computador

2. Se o cartão SD tiver quaisquer arquivos ou pastas nele, copie tudo para uma pasta no seu computador

3. Execute o aplicativo Disk Utility

4. Selecione seu cartão SD no painel da esquerda

   ::: danger

   Certifique-se de escolher o dispositivo correto, caso contrário você pode apagar a unidade errada acidentalmente!

   :::

5. Clique em "Partition" no topo
   - If "Partition" does not appear, make sure to choose the device instead of a volume

6. Certifique-se de que "Partition Layout" está definido para "1 Partition"

7. Digite qualquer coisa no campo "Name"

8. Certifique-se de que "Format" está definido como "MS-DOS (FAT)"

9. Clique em "Options" abaixo da tabela de partição

10. Escolha "Master Boot Record"

11. Clique em "OK"

12. Clique em "Apply"

13. Clique em "Partition"

14. Aguarde a conclusão da formatação

15. Feche o Disk Utility

16. Se o cartão SD tinha quaisquer arquivos ou pastas nele, copie tudo de volta para o SD do seu computador

## Troubleshooting

- SD card remains undetected by console or continues to display the wrong capacity after formatting
  - Your SD card may be partitioned or have unallocated space. Siga as instruções [aqui](https://wiki.hacks.guide/wiki/SD_Clean/Mac) para reformatar o seu cartão SD.