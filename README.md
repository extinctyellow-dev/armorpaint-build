# ArmorPaint Windows x64 - compilação automática no GitHub Actions

Este repositório usa um computador Windows do GitHub Actions para baixar o código-fonte oficial do ArmorPaint, compilar a versão Windows x64 e entregar um artefato chamado `ArmorPaint-Windows-x64`.

## Como usar

1. Abra a aba **Actions**.
2. Clique em **Build ArmorPaint Windows x64**.
3. Clique em **Run workflow**.
4. Aguarde o job terminar.
5. Abra a execução concluída e baixe **ArmorPaint-Windows-x64** em **Artifacts**.
6. Extraia o ZIP e execute `ArmorPaint.exe`.

## O que o workflow faz

- usa `windows-2022`;
- baixa o repositório oficial `armory3d/armorpaint`;
- garante LLVM/`clang-cl`;
- gera o projeto Visual Studio pelo script oficial;
- compila em Release x64;
- procura automaticamente a pasta de runtime;
- monta uma pasta portátil com `ArmorPaint.exe` e `data/`;
- salva o hash exato do commit do ArmorPaint;
- publica o resultado como artifact por 7 dias.

> O código do ArmorPaint vem diretamente do projeto oficial e permanece sujeito à licença do projeto original.
