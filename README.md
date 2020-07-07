# XamarinErrors

Repositorio com Ajuda para de Possiveis Problemas com Xamarin

# Xamarin.Forms

### Erro The “DebugType” parameter is not supported by the “XamlCTask” task. Verify the parameter exists on the task, and it is a settable public instance property.

Esse erro geralmente acontece quando alguma versão do Xamarin.Forms é diferente das outras. Geralmente é resolvido consolidando as versões .No visual studio clique em Manage NuGet Packages for Solution, na aba update atualize os pacotes Xamarin.Forms de Todos os projetos


# Xamarin.Android

### 1. Atualizando Referencias do Xamarin.Android

1 - Remova os Pacotes do Projeto Android, os Xamarin.Android , Xamarin.Forms e Xamarin.Essentials

2 - Instale os Pacotes na Ordem

* Xamarin.Android.Support.Annotations
* Xamarin.Android.Support.Compat
* Xamarin.Android.Support.Core.UI
* Xamarin.Android.Support.Core.Utils
* Xamarin.Android.Support.Fragment
* Xamarin.Android.Support.Media.Compat

Caso seja necessario ( e utilize os pacotes abaixo) os atualize

* Update Xamarin.Android.Support.Design
* Update Xamarin.Android.Support.v7.AppCompat
* Update Xamarin.Android.Support.v4
* Update Xamarin.Android.Support.v7.CardView
* Update Xamarin.Android.Support.v7.MediaRouter

Em seguida instale o Xamarin.Forms e Xamarin.Essentials.

### 2. Erro : xamarin java.security.cert.CertPathValidatorException: Trust anchor for certification path not found.

Adicione System.Net.ServicePointManager.ServerCertificateValidationCallback += (o, cert, chain, errors) => true; No MainActivity.cs.


# Xamarin.iOS

### 1. UIWebView Deprecation

Este é o famoso erro que recebemos ao subir um App na Appstore :

ITMS-90809: Deprecated API Usage – Apple will stop accepting submissions of apps that use UIWebView APIs. See https://developer.apple.com/documentation/uikit/uiwebview for more information.

After you’ve corrected the issues, you can use Xcode or Application Loader to upload a new binary to App Store Connect.

Enquanto o time do Xamarin altera o Xamarin.Forms para resolver , é possivel utilizar uma solução simples.

1 - Acesse as propriedades do projeto iOS -> iOS Build -> e no campo additional mtouch arguments , adicione : --optimize=experimental-xforms-product-type

O Artigo completo explicando : https://devblogs.microsoft.com/xamarin/uiwebview-deprecation-xamarin-forms/

Artigo Pt-BR com apanhado de dicas caso a solução 1 não seja suficiente: https://bit.ly/itms90809

### 2. Erro ao parear Visual Studio no Windows com um MacOS

Acontece este erro ao tentar parear pela primeira vez o VS com o MacOS: 
"unable to authenticate with ssh keys. Please try to login with credentials first pair mac"

1 - Execute este comando no terminal do mac: sudo chmod -R 755 ./ ls -l .ssh

### Este Repositorio esta em desenvolvimento .. ;)

Pull Requests são bem vindos :D


