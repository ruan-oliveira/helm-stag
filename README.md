# Repositórios de Helm Charts

O objetivo desse repositório é a centralização e guarda dos Helm Charts desenvolvidos para aplicações e componenetes dos softwares corporativos.

## Estrutura padrão

O repositório está estruturado da seguinte forma:

```dir
charts
  <Applications charts>
    Chart.yaml
    values.yaml
    ...
README.md
```

## Principais entradas

- Values
- Chart
- Release

## Como buscar um parâmetro

Sempre comece com duplas chaves.

```
{{ bucar aqui dentro }}
```

- Por exemplo:

```
{{ .Values.image.repository }}
```

## Comandos

Como examinar seu chart

```cmd
helm lint <seu chart>
```

Simulador de instalação ou atualização

```cmd
helm install <release> <chart> --dry-run
```

```cmd
helm upgrade <release> <chart> --dry-run
```

Fazer download de um chart remoto

```cmd
helm pull estag/wordpress
```