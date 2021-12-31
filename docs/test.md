---
icon: material/alert-outline
---

## Links

### 내부 문서

```markdown
- [live preview](../#live-preview)
- [tables](#tables)
- [Reference](../reference)
```

- [live preview](../#live-preview)
- [tables](#tables)
- [Reference](../reference)

### URL

마크다운 기본 문법은 `<` `>` 을 이용해서 URL을 감싸는 것이라고 한다.

github 처럼 자동으로 link 가 생성되게 하려면 [MagicLink](https://facelessuser.github.io/pymdown-extensions/extensions/magiclink/)
extension 을 설정해줘야 한다.

```markdown
<https://facelessuser.github.io/pymdown-extensions/extensions/magiclink/>
```

<https://facelessuser.github.io/pymdown-extensions/extensions/magiclink/>


## Abbreviations

`HTML`이나 `W3C` 위에 마우스를 위치하면 간단한 설명이 나옵니다.

```md
The HTML specification is maintained by W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
```

The HTML specification is maintained by W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium


## Admonitions

!!! note
    test
    note test


??? example "test"
    hahahahaha
    ```
    ??? example
    ```


??? bug
    collapsed?

???+ danger
    ```
    test 1 2 3 4
    ???+ note
    ```
    `tip`, `success`, `done`, `help`, `warning`, `info`, `abstract`, `failure`, `bug`, `example`

## CodeBlock

### code title
```py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### add annotation
`+` 를 클릭하면 설명을 볼 수 있습니다.

``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be expressed in Markdown.


### adding line numbers

``` py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### highlighting lines
``` py hl_lines="2 4"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### highlighting inline code blocks
```md
The `#!python range()` function is used to generate a sequence of numbers.
```

The `#!python range()` function is used to generate a sequence of numbers.

### include src file
이 기능은 해당 repo 에 있는 파일만 포함 할 수 있습니다.

```python linenums="1" hl_lines="11 24-26" title=".github/workflows/deploy-mkdocs.yml"
--8<-- ".github/workflows/deploy-mkdocs.yml"
```


### tabs

=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```


### list with tabs
=== "Unordered list"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

## Images
### left align
```md
![image](https://dummyimage.com/600x400/eee/aaa)
```

![image](https://dummyimage.com/600x400/eee/aaa)

```md
![Image title](https://dummyimage.com/600x400/eee/aaa){ width="300" align=left }
```

![Image title](https://dummyimage.com/600x400/eee/aaa){ width="300" align=left }

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

![Image title](https://dummyimage.com/600x400/eee/aaa){ width="300" align=right }
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

```md
![Cat](https://static.boredpanda.com/blog/wp-content/uploads/2019/07/1-5d2cd2a0ac058__880.jpg){width="300" : .zoom .shadow .center}

![Cat](https://static.boredpanda.com/blog/wp-content/uploads/2019/07/1-5d2cd2a0ac058__880.jpg){width="300" : .shadow .no-border}
```

![Cat](https://static.boredpanda.com/blog/wp-content/uploads/2019/07/1-5d2cd2a0ac058__880.jpg){width="300" : .zoom .shadow .center}

![Cat](https://static.boredpanda.com/blog/wp-content/uploads/2019/07/1-5d2cd2a0ac058__880.jpg){width="300" : .shadow .no-border}







## Tables

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |


| Method      | Description                          |
| ----------: | -----------------------------------: |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |

## Lists

### definition list

`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

### task view
- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque



## MathJax

```markdown
$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$
```

$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$


## Footnotes

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
