# XamarinErrors

Repositorio com Configurações de Possiveis Problemas com Xamarin

# Xamarin.Forms

### Erro The “DebugType” parameter is not supported by the “XamlCTask” task. Verify the parameter exists on the task, and it is a settable public instance property.

Esse erro geralmente acontece quando alguma versão do Xamarin.Forms é diferente das outras. Geralmente é resolvido consolidando as versões .No visual studio clique em Manage NuGet Packages for Solution, na aba update atualize os pacotes Xamarin.Forms de Todos os projetos


# Xamarin.Android

### Atualizando Referencias do Xamarin.Android

1 - Remova os Pacotes do Projeto Android, os Xamarin.Android , Xamarin.Forms e Xamarin.Essentials

2 - Instale os Pacotes na Ordem

Xamarin.Android.Support.Annotations
Xamarin.Android.Support.Compat
Xamarin.Android.Support.Core.UI
Xamarin.Android.Support.Core.Utils
Xamarin.Android.Support.Fragment
Xamarin.Android.Support.Media.Compat

Caso seja necessario ( e utilize os pacotes abaixo) os atualize

Update Xamarin.Android.Support.Design
Update Xamarin.Android.Support.v7.AppCompat
Update Xamarin.Android.Support.v4
Update Xamarin.Android.Support.v7.CardView
Update Xamarin.Android.Support.v7.MediaRouter

Em seguida instale o Xamarin.Forms e Xamarin.Essentials.


### Este Repositorio esta em desenvolvimento .. ;)



