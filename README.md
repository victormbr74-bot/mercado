# Mercato

Lista de compras offline, instalável e com versão Android nativa.

## Web

Abra `index.html` localmente ou publique o conteúdo no GitHub Pages. O workflow de Pages monta o site, compila o APK e disponibiliza `downloads/mercato.apk`; o botão **Baixar APK** da página inicial usa esse endereço.

## Android

O app Android é uma casca nativa leve que carrega a mesma experiência da web a partir dos assets locais, mantendo as listas no armazenamento do aparelho. O projeto usa Gradle e Android Gradle Plugin; a compilação automática é feita pelo workflow `.github/workflows/deploy-pages.yml`.

Para compilar localmente, é necessário ter Java 17, Android SDK (API 35) e Gradle 8.11.1 instalados:

```text
gradle :app:assembleRelease
```

O APK resultante fica em `app/build/outputs/apk/release/app-release.apk` e usa o ícone próprio em `app/src/main/res/drawable/mercato_icon.png`.

## iOS

iPhone não instala APK. O formato equivalente é IPA, que precisa ser compilado e assinado com Xcode em macOS e uma conta Apple. A versão web/PWA já funciona no iPhone pelo Safari; um IPA só deve ser criado quando houver um ambiente Apple e credenciais de assinatura disponíveis.
