## Factory

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
      <td>26/10/2020</td>
      <td>
        Fábio Teixeira(<a target="blank" href="https://github.com/fabio1079">fabio1079</a>)
      </td>
      <td>Adicionando utilização do factory no projeto</td>
      <td>0.1</td>
    </tr>
    <tr>
      <td>26/10/2020</td>
      <td>
        Lucas Midlhey(<a target="blank" href="https://github.com/lucasmidlhey">lucasmidlhey</a>)
      </td>
      <td>Aplicabilidade</td>
      <td>0.2</td>
    </tr>
    <tr>
      <td>26/10/2020</td>
      <td>
        Cauê(<a target="blank" href="https://github.com/caue96">caue96</a>)
      </td>
      <td>Incrementando a introdução do que é o padrão factory</td>
      <td>0.3</td>
    </tr>
  </tbody>
</table>

## Introdução

<p align="justify">&emsp;
O Factory é um padrão criacional de projeto que fornece uma interface para criar objetos em uma superclasse, mas permite que as subclasses alterem o tipo de objetos que serão criados.
</p>
<p align="justify">&emsp;
O padrão Factory sugere que seja substituido chamadas diretas de construção de objetos por chamadas para um método especial. A mudança de chamada do construtor passa de uma parte do programa para outra, agora pode sobrescrever o método em uma subclasse e alterar as classes que estão sendo criados pelo método.
</p>

## Estrutura

![Estrutura Strategy](../../images/design_patterns/factory.png)

## Aplicações no Projeto(QRodízio)

### Disclaimer

Primeiramente é bom deixar claro que nosso projeto está utilizando de linguagens multi-paradigmas(python e javascript) sendo assim, adaptações aos padrões são necessárias para não fugir do estilo do código utilizado.

A Linguem python possui em seu "zen of python" a seguinte declaração: "Simple is better than complex". Seguindo a filosifia do "zen of python" **decidimos que, se algo pode ser feito em uma função, então será feito em uma função**.

### Utilização

Em nossa base de código o padrão factory é utilizado para definir qual estratégia de verificação de autorização de usuário será utilizada

Segue um exemplo de uso do padrão factory em [authentication](https://github.com/UnBArqDsw/2020.1_G10_QRodizio_Backend/blob/develop/qrodizio/ext/authentication.py):

```python
def _role_check(func, employee, role, *args, **kwargs):
    """Check user permission based on its role"""
    checker = permission_strategy_factory(role)

    if checker(employee):
        return func(current_employee=employee, *args, **kwargs)
    else:
        raise UserUnauthorizedException(403)


def permission_strategy_factory(role):
    """Given a role, returns a permission strategy for that role"""
    if role == EmployeeRole.basic:
        return basic_permission_strategy
    elif role == EmployeeRole.manager:
        return manager_permission_strategy
    else:
        return no_permission_strategy
```

## Aplicabilidade

Use o Abstract Factory quando seu código precisa trabalhar com diversas famílias de produtos relacionados, mas que você não quer depender de classes concretas daqueles produtos-eles podem ser desconhecidos de antemão ou você simplesmente quer permitir uma futura escalabilidade.

O Abstract Factory fornece a você uma interface para a criação de objetos de cada classe das famílias de produtos. Desde que seu código crie objetos a partir dessa interface, você não precisará se preocupar em criar uma variante errada de um produto que não coincida com produtos já criados por sua aplicação.

## Referências

<ul>
<li>
REFACTORING.GURU. Strategy. Disponível em: https://refactoring.guru/pt-br/design-patterns/factory-method . Acesso em: 26 de outubro. 2020.
</li>
</ul>
