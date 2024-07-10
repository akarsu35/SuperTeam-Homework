# Solana Akıllı Sözleşme Etkileşim Projesi

Bu proje, TypeScript ve Anchor kullanarak bir Solana akıllı sözleşmesiyle nasıl etkileşimde bulunulacağını gösterir.

## Proje Kurulumu

1. Proje dizinini oluşturun ve bu dizine gidin:
    ```bash
    mkdir homework
    cd homework
    ```

2. Projeyi başlatın:
    ```bash
    yarn init -y
    code .
    ```

3. Bağımlılıkları ekleyin:
    ```bash
    yarn add @types/node typescript @solana/web3.js @project-serum/anchor
    yarn add -D ts-node
    ```

4. TypeScript yapılandırmasını başlatın:
    ```bash
    yarn tsc --init --rootDir ./ --outDir ./dist --esModuleInterop --lib ES2020 --module commonjs --resolveJsonModule true --noImplicitAny true
    ```

5. Proje dosyalarını oluşturun:
    ```bash
    touch call_program.ts counter_idl.ts wallet.json
    ```
6. package.json içersine ekleyin:
    ```bash
    "scripts": {
    "call_program": "ts-node ./call_program.ts"},
    ```

## Proje Dosyaları

- **counter_idl.ts**: Akıllı sözleşmenin IDL (Arayüz Tanım Dili) dosyasını içerir.
- **call_program.ts**: Akıllı sözleşme ile etkileşim kurmak için kullanılan betik dosyasını içerir.
- **wallet.json**: Cüzdanın gizli anahtarını tamsayı dizisi formatında içerir.


## yarn call_program
7. terminalde **yarn call_program** çalıştırın:

    ```bash
    **örnek bir çıktılar.**
    Transaction signature:3fZ47WACptkd1zhg7uoLqT4BpRyUozmj8cQaSFm5vMkY6PhJr3UKM72KGkxgm56Mxre1oo9oFxiCzGF4h5ak56e1
    Counter incremented

    Transaction signature: wVEiV6TNa8TkXdesN7QhwYvBvLGJx2zr49z7x5vsjZguSyiE9grUjH552AWjCNC53BRPrrGKjtWAJfnfETenopC
    Counter set to 5

    Transaction signature: ndgHvDPAS1Cc7bdZARyWzbxo1gSfwGzZTEmacsPHYwB4rFM332rghRUt8PT7jiteAUYTFBXsUFiK3tBUtNv67pP
    Counter decremented
    ```
