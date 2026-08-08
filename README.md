# Praça do Rosário — Cadastro Georreferenciado Piloto

Projeto piloto de levantamento e publicação de informações georreferenciadas da **Praça do Rosário, em Lagarto-SE**.

A proposta é demonstrar, em pequena escala, um fluxo completo de cadastro territorial utilizando ferramentas livres e de baixo custo, desde a coleta e edição dos dados até a disponibilização de um mapa web interativo.

## Objetivo

Construir uma base geográfica editável e atualizável da praça, permitindo o registro e a visualização de elementos físicos e ambientais do espaço urbano.

O projeto também funciona como prova de conceito para futuros levantamentos de arborização urbana e inventários de espaços públicos.

## Escopo do piloto

O levantamento contempla, progressivamente:

- limite da praça;
- áreas e canteiros;
- pavimentos e espaços de circulação;
- mobiliário urbano;
- elementos lineares;
- árvores e demais elementos de arborização;
- fotografias e atributos associados às feições.

## Tecnologias utilizadas

- **QGIS** — edição, organização e análise dos dados geográficos;
- **GeoPackage (`.gpkg`)** — armazenamento das camadas vetoriais;
- **GeoTIFF (`.tif`)** — ortofoto utilizada como referência;
- **QField** — coleta e atualização de dados em campo pelo celular;
- **qgis2web** — conversão do projeto QGIS para mapa web;
- **Leaflet** — biblioteca utilizada na visualização web;
- **GitHub Pages** — hospedagem gratuita do mapa público.

## Sistema de referência

Os dados de trabalho são organizados em:

**SIRGAS 2000 / UTM Zona 24S — EPSG:31984**

Esse sistema permite trabalhar diretamente com medidas métricas de distância e área.

## Estrutura das camadas

O cadastro é organizado principalmente nas seguintes camadas:

- `praca` — limite da praça;
- `areas` — canteiros, gramados, pavimentos e outras áreas;
- `elementos_lineares` — meios-fios, grades, drenagem e outros elementos lineares;
- `mobiliario` — bancos, lixeiras, postes, placas e equipamentos;
- `arvores` — cadastro arbóreo georreferenciado.

As camadas vetoriais são armazenadas em um único arquivo GeoPackage.

## Fluxo de trabalho

```text
Ortofoto
   ↓
QGIS
   ↓
GeoPackage
   ↓
QField
   ↓
Coleta em campo
   ↓
QGIS
   ↓
qgis2web
   ↓
GitHub Pages
   ↓
Mapa público / QR Code
```

## Publicação

O mapa é exportado pelo **qgis2web** e publicado como aplicação web estática no **GitHub Pages**.

Isso permite manter um endereço permanente para acesso público, enquanto os dados podem continuar sendo atualizados no projeto original e republicados sem alteração do QR Code.

## Status

🚧 **Projeto em desenvolvimento**

A primeira etapa corresponde à digitalização das feições visíveis na ortofoto.  
As etapas seguintes incluem coleta em campo com QField, registro fotográfico, inventário arbóreo e publicação da versão completa do mapa.

## Natureza do projeto

Este é um **projeto piloto independente**, desenvolvido como demonstração técnica de um fluxo de cadastro georreferenciado de espaços públicos utilizando ferramentas SIG e tecnologias web.
