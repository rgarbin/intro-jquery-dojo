# Introdução ao jQuery

- Esta apresentação foi elaborada após ler o livro do Maujor, "Jquery a Biblioteca do Programador JavaScript"
- O objetivo foi apresentar em um encontro técnico para troca de conhecimento.
- Recomendo muito comprar: http://www.livrojquery.com.br/

## O que é o jQuery?
- É uma biblioteca projetada para mudar a forma como escrevemos javascript.
- Teve inicio em 2005 com um artigo de John Resig
- Livre e aberto, pode ser utilizado para desenvolvimento pessoal e comercial
- Seu slogan é: "ESCREVA MENOS E FAÇA MAIS"

Segundo John Resig, o criador:

    O foco principal da biblioteca jQuery é simplicidade.
    Por que submeter os desenvolvedores ao martírio de escrever códigos longos e complexos para criar simples efeitos.

## Evolução
- 2005 - Inicio
- 2006 - Primeiro Plugin
- 2007: Versões 1.1, 1.1.1, 1.1.2, 1.1.3a, 1.1.3.1, 1.1.4, 1.2, e 1.2.1
- 2008: Versões 1.2.2, 1.2.3, 1.2.4, 1.2.5, e 1.2.6
- 2009: Versões 1.3, 1.3.1 e 1.3.2
- 2010: Versões 1.4, 1.4.1, 1.4.2, 1.4.3, 1.4.4
- 2011: Versões 1.5, 1.5.1, 1.5.2, 1.6, 1.6.1, 1.6.2, 1.6.3, 1.6.4, 1.7 e 1.7.1
- 2012: Versões 1.7.2, 1.8.0, 1.8.1, e 1.8.2
- 2013: Versões 1.9.0 e 2.0.0 com a remoção do suporte ao IE6-8)

## Quem usa?
- Google
- Dell
- Bank of America
- Digg
- NBC
- CBS News
- Netflix
- Mozilla.org
- Wordpress
- Entre vários outros grandes. Etc...

## Vantagens
- Não precisa ser um profundo conhecedor de javascript para iniciar
- Simplicidade é a palavra-chave que resume e nortea o desenvolvimento com jQuery
- jQuery foi criado com a preocupação de estar em conformidade com os padrões web
- Compatibilidade entre diversos navegadores
- Admite programação encadeada, ou seja, cada método retorna um objeto
- É extensível, pois permite criação e inserção de novas funcionalidades
- Redução de código
- vasta documentação
- Leve
- Suporte a Ajax
- Não é preciso instalar nada para utilizar
- Agilidade

## Como usar?
- Barbadinha, basta fazer o download e linkar o arquivo a sua página
- Durante o download irá notar que exitem dois formatos
    - Uncompressed(Ideal para desenvolvedores que vão trabalhar na biblioteca.)
    - Minified(Ideal para o ambiente de produção.)

## Conflitos
- Atenção, jQuery não é a unica bibliteca javascript
    - Prototype
    - Mootools
    - YUI
    - Dojo
- jQuery utiliza por default o construtor $(), mas ele não é o único!
- Tudo o que é escrito em jQuery utiliza o construtor
- Para evitar conflitos utilize o alias "jQuery" ou defina qual será seu construtor

## Eventos
Uma das frases do livro que acho mais incrível no livro do Maujor é esta:

    É licito dizer que se não houvesse eventos, simplesmente não haveria javascript

O jQuery permite e recomenda a separação de marcação(HTML), comportamento(JS) e apresentação(CSS), deixando nosso código clean
Dois dos principais eventos sem dúvida são o ready() e o load():

    jQuery(document).ready(function(){ // DOM ok
      jQuery(window).load(function(){
        alert('Página Carregada, bora baixar as imgs?');
      });
    });


## Seletor 
- Seletores servem para encontrar elementos na nossa página
- Utiliza os seletores do CSS 3, e mais alguns particulares
- Existem diversos tipos de seletores, tudo depende do que você precisa!
    - Seletor por ID: jQuery('#seletorElemento1').css('color', 'red');
    - Seletor pelo atributo CLASS: jQuery('.classInter').css('color', 'red');
    - Seletor por elemento: jQuery('div').each( function(){  alert(jQuery(this).text()); });
    - Seletor por tipo: Query(':checkbox').attr('checked', true);


## Filtros
Com jQuery podemos aplicar filtros para os seletores
Os filtros nos ajudam a ser mais precisos em nossa buscas, como por exemplo:

    jQuery('li:first').hide();
    jQuery('li:last').hide();
    jQuery('li:even').hide();
    jQuery('li:odd').hide();
    jQuery('li:eq(6)').hide();
    jQuery('li:has(p)').hide();
    jQuery('li:not(li:first)').hide();


## Exemplos
- jQuery faz por merecer seu slogan

Veremos como marcar todas as checkbox do formulário:

    for (indice=0; indice<document.forms.length; indice++) {
      for (i=0; i<document.forms[indice].elements.length; i++) {
        if ((document.forms[indice].elements[i].type == 'checkbox')) {
          document.forms[indice].elements[i].checked = true;
        }
      }
    }

    jQuery(document).ready(function() {
      jQuery(':checkbox').attr('checked', true);
    });


Agora veremos como setar o foco no primeiro elemento do formulário:

    for (indice=0; indice<document.forms.length; indice++) {
      for (i=0; i<document.forms[indice].elements.length; i++) {
        if ((document.forms[indice].elements[i].type == 'text')) {
          if ((document.forms[indice].elements[i].disabled == 'false') && (document.forms[indice].elements[i].readonly == 'false')) {
            setTimeout('document.forms[indice].elements[i].focus()',500);
            break;
          }
        }
      }
    }

    $(function(){
      $(':text:visible:enabled[value=""]:first').focus();
    });


## Conclusão
O uso do JQuery torna nosso trabalho mais simples e ágil, fazendo com que os desenvolvedores ganhem tempo e não percam o foco.
Não achem que jQuery é uma bala de prata, infelizmente não existe solução perfeita para tudo, mas em muito casos será um bom amigo!

## Vídeos da BlueSoft! 
- jQuery - Trabalhando com eventos(http://vimeo.com/18702701)
- jQuery - Funções de animação(http://vimeo.com/19042175)
- jQuery - Funções utilitárias(http://vimeo.com/19978558)
- jQuery - Funções utilitárias para Ajax(http://vimeo.com/20649896)
- jQuery - Plugins de interação(http://vimeo.com/23554739)
- jQuery Ui - http://vimeo.com/21608008
- jQuery Ui - http://vimeo.com/22397630

