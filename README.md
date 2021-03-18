# Utils
Funções úteis para não esquecer!

# Tabela de conteúdos
<!--ts-->
   * [React](#react)
<!--te-->

# React
### Converter dados em JSON e fazer download
```
var htmlElement = document.createElement("a");
var stringJson = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(meusDadosParaConverterEmJson));
htmlElement.setAttribute("href", stringJson);
htmlElement.setAttribute("download", "meusDadosConvertidos.json");
document.body.appendChild(htmlElement);
htmlElement.click();
document.body.removeChild(htmlElement);
```
