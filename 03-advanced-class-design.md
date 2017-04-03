
    Develop code that uses abstract classes and methods
    Develop code that uses the final keyword
    Create inner classes including static inner class, local class, nested class, and anonymous inner class
    Use enumerated types including methods, and constructors in an enum type
    Develop code that declares, implements and/or extends interfaces and use the @Override annotation.
    Create and use Lambda expressions


@Override pode ser usado em:
- métodos implementados de uma interface
- métodos sobrescritos da classe mãe que não sejam final
- métodos de Object

equals:
- x.equals(x) == true
- x.equals(y) == y.equals(x)
- x.equals(y) && y.equals(z) -> x.equals(z)
- x.equals(y) consistente se não mudar o estado
- x.equals(null) == false

hashcode:
- se sobrescre equals, sobrescreve hashcode
- o resultado não deve mudar com a mudança do estado do objeto
- x.equals(y) == true -> x.hashcode() == y.hashcode()
- x.equals(y) == false não -> x.hashcode() != y.hashcode(), podem ser iguais
- usa as mesmas variáveis do equals ou menos

enums:
- membros static final
- NomeEnum.values(), membroEnum.ordinal(), membroEnum.name()
- não compara com int
- só converte com String exata NomeEnum.valueOf("STRING") senão solta IllegalArgumentException
- não tem herança mas pode implementar interfaces
- pode ser utilizado em switch
- switch(enum) não coloca o tipo no case, só o valor do membro. Não compila se colocar
- pode ter construtor, atributos e métodos
- ; obrigatório se tiver outras coisas além dos membros
- membros sempre primeiro
- construtor sempre private (se não colocar modificador ele considera private)
- construtor só roda uma vez
- aceita métodos abstratos
