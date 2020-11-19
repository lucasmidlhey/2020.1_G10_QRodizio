# Reutilização

## Histórico de Versão

<table>
  <thead>
    <tr>
      <th>Data</th>
      <th>Autor(es)</th>
      <th>Descrição</th>
      <th>Versão</th>  
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>19/11/2020</td>
      <td>
        Caio César Beleza(<a target="blank" href="https://github.com/Caiocbeleza">Caiocbeleza</a>)
      </td>
      <td>Adicionando Introdução de reutilização de software</td>
      <td>0.1</td>
    </tr>
    <tr>
      <td>19/11/2020</td>
      <td>
        Joao Pedro(<a target="blank" href="https://github.com/Caiocbeleza">jppgomes</a>)
      </td>
      <td>Adicionando exemplo de reutilização</td>
      <td>0.2</td>
    </tr>

  </tbody>
</table>

## Introdução

<p align="justify">&emsp;
A reutilização de software é baseada na utilização de conceitos, produtos ou soluções previamente elabolaras para a criação de um novo software. Podem ser reutilizadas partes de um sistema que já desenvolvido, como especificações, arquitetura e código fonte.
</p>
<p align="justify">&emsp;
A reutilização pode auxiliar numa redução de tempo no desenvolvimento de um novo software, consequentemente também reduzindo os custos. Por isso, no cenário atual de desenvolvimento ágil de software, é um conceito interessante.
</p>
<p align="justify">&emsp;
Portanto, os tópicos a seguir descrevem as partes reutilizáveis do projeto QRodízio, que foram feitas com o objetivo de facilitar tanto a manutenção do sistema, quanto o potencial de evolução dele.
</p>

## Arquitetura

## Código

<ul>
<li>
[Style.css](https://github.com/UnBArqDsw/2020.1_G10_QRodizio_Frontend/blob/tables-and-qrcodes/src/assets/styles/styles.css) : O arquivo que contém os estilos utilizados no projeto. É um bom exemplo de reutilização, pois cada estilo definido pode ser acessado e aplicado em vários elementos do sistema, o que diminui repetições e facilita a mudança de estilo dos elementos, já que podem ser mudados vários elementos de uma vez, ao invés de ter que mudar de um por um.
</li>

<li>
[builders.py](https://github.com/UnBArqDsw/2020.1_G10_QRodizio_Backend/blob/develop/qrodizio/builders.py)Este exemplo onde é utilizado o padrão builder ilustra como você pode reutilizar o mesmo código de construção de objeto.
</li>

</ul>

## Referências

<ul>
<li>

DEVMEDIA. Reutilização de Software - Revista Engenharia de Software Magazine 39. Disponível em:  https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956. Acesso em: 19 de novembro. 2020.

</li>
</ul>