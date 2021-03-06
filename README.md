Android-CepView
===============

**CepView** - **Android Cep View** é um Android UI widget com os principais campos relacionados a endereço (CEP, endereço, número, complemento, bairro, cidade, estado), fornece preenchimento automático dos dados com base no **CEP (Código de Endereçamento Postal)** informado.

####Funcionamento
Após o preenchimento do campo do número do CEP e perda do foco é feita uma busca na API informada ou, por padrão, na API [CorreioControl do Aviso Brasil](http://avisobrasil.com.br/correio-control/api-de-consulta-de-cep/) e, caso o CEP seja encontrado, os campos Endereço, Bairro, Cidade e Estado são preenchidos com os valores retornados.<br>
Tudo isso de forma transparente para o programador e visualmente elegante para o usuário, uma vez que durante a busca é mostrado um *ProgressBar* indicando que a pesquisa está sendo feita.

###Características
* Campos Disponíveis
  * **Cep** - campo de texto para preenchimento do número do CEP. Após a perda do foco o valor é verificado numa API de CEP e os outros campos são modificados.
  * **Endereço** - campo de texto para preenchimento do Endereço, podendo ser rua, avenida, etc.
  * **Número do Endereço** - campo de texto para preenchimento do Número do endereço.
  * **Complemento** - campo de texto para preenchimento do Complemento ao endereço.
  * **Bairro** - campo de texto para preenchimento do Bairro.
  * **Cidade** - campo de texto para preenchimento da Cidade.
  * **Estado** - spinner (combobox) para seleção do Estado.

###Compatibilidade
Compatível com Android 2.2 ou superior.

###Tecnologias Utilizadas
* Android
* Gson - Biblioteca para conversão simples de **JSON** para **Java** e vice-versa.
* API de CEP [CorreioControl do Aviso Brasil](http://avisobrasil.com.br/correio-control/api-de-consulta-de-cep/). ~~Esta API pode ser modificada, assim o usuário pode usar a sua própria API.~~

###Como usar
**CepView** é um [Library Project](http://developer.android.com/guide/developing/eclipse-adt.html#libraryProject), basta adicionar como referência em Library do seu projeto pelo eclipse.<br>
Adicione ao arquivo `AndroidManifest.xml` as seguintes permissões:
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```
Crie um componente `com.arthurassuncao.cepview.CepView` em um *layout*, como o exemplo abaixo:
```xml
<com.arthurassuncao.cepview.CepView
  android:id="@+id/cep_view_exemplo"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content" />
```
Pronto, Enjoy it.

###Desenvolvedor
* Arthur Nascimento Assuncao

###License
Copyright (c) 2013, Arthur Nascimento Assuncao
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
