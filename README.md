### Generics

```java
Lista<String>minhaLista = new Lista<>();

public class Lista<T>{
    private T t;
}
```

#### Contexto:

- Evitar casting execessivo
- Evitar códigos redundantes
- Econtrar erros em tempo de compilação
- Introduzido desde o Java SE 5.0

#### Wildcards

- Unknown Wildcards(Unbounded)	

  - ```java
    public void impremeList(List<?>lista){
    	for(Object obj : lista){
    		System.out.println(p);
    	}
    }
    List<Aluno>minhaLista = new List<Aluno>();
    imprimeLista(minhaLista);
    ```

- Bounded Wildcard(Upper Bounded)

  - ```java
    public void impremeLista(List<? extends Pessoa> listaPessoas){
    	for(Pessoa p : listaPessoas){
    		System.out.println(p);
    	}
    }
    List<Aluno>minhaLista = new List<Aluno>();
    imprimeLista(minhaLista);
    ```

    

- Bounded Wildcard(Lower Bounded)

  - ```java
    public void impremeLista(List<? super Pessoa> listaPessoas){
    	for(Pessoa p : listaPessoas){
    		System.out.println(p);
    	}
    }
    List<Aluno>minhaLista = new List<Aluno>();
    imprimeLista(minhaLista);
    ```

    

#### Convenção

- **K** para "key", exemplo : `Map<K,V>`
- **V** para "Value", exemplo : `Map<K,V>`
- **E** para "Element", exemplo : `List<E>`
- **T** para "Type", exemplo : `Collections#addAll`
- **?** quando genérico

