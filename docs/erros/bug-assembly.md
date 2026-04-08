# Comportamentos estranhos da STM32CubeIDE

**A IDE abre um arquivo Assembly após gravar o programa**

Em algumas versões da STM32CubeIDE, especialmente da linha 2.1.x, ao iniciar o debug a IDE pode abrir automaticamente um arquivo como startup_stm32xxxx.s.

Isso pode dar a impressão de que algo deu errado.

---

## O que isso significa

Na prática, muitas vezes esse comportamento é apenas visual. O programa pode ter sido gravado normalmente e estar executando na placa.

---

## O que fazer

Antes de assumir que houve erro:

- verifique se o código realmente foi gravado;
- observe o comportamento da placa;
- confira se o LED está piscando ou se o programa esperado está rodando.

Se tudo estiver funcionando, esse comportamento pode ser ignorado.

---

## Arquivo .ioc abrindo como XML

O arquivo .ioc é o arquivo de configuração gráfica do projeto STM32. Em alguns casos, a IDE pode abrir esse arquivo como texto ou XML, em vez de mostrar a interface visual do CubeMX.

---

## Solução

Clique com o botão direito sobre o arquivo .ioc e escolha:

```
Open With -> Device Configuration Tool
```

Isso normalmente restaura a abertura correta do configurador gráfico.
