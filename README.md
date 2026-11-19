# OpenCode Nexus

Launcher e gerenciador de conexao do [OpenCode](https://opencode.ai) para Windows 10 e 11.

Fecha o app antes de mexer na rede, sobe WARP, Tor, VPN, WireGuard, VPN Gate ou proxy, confere se o modelo voltou a responder e reabre na mesma conversa. Troca o IP quando o limite gratuito chega. Cuida do banco sem apagar conversa nenhuma.

## Baixar

Pegue `OCNexus.exe` na [ultima release](../../releases/latest). Nao precisa de Python nem de instalador: um arquivo, duplo-clique.

Deixe o `OCNexus.exe` numa pasta fixa, como `Documentos\OC Nexus`. O atalho e a atualizacao apontam para onde o arquivo esta; mover o `.exe` depois deixa o atalho antigo sem destino.

O Windows vai avisar que o aplicativo nao tem assinatura digital. E o preco de distribuir um `.exe` sem certificado. O download e por HTTPS e cada release publica o SHA-256 em `SHA256SUMS.txt`; para conferir:

```powershell
Get-FileHash .\OCNexus.exe -Algorithm SHA256
```

Alguns antivirus reclamam de qualquer executavel empacotado com PyInstaller, mesmo sem infeccao. Confira o SHA-256 e, se bater com o da release, adicione uma excecao para o arquivo.

Compare com a linha de `OCNexus.exe` no arquivo de somas da mesma release.

## Atualizacao

O programa confere a ultima release ao abrir e mostra uma tela quando ha versao nova: versao instalada, publicada, tamanho do download e as notas. `[1]` atualiza, `[2]` continua e `[0]` sai. A conferencia roda no maximo a cada seis horas e, na abertura, usa so o resultado ja guardado: sem internet o programa abre no mesmo tempo.

O download so e aceito com o SHA-256 publicado na release. Quando a release marca uma versao minima, a opcao de continuar desaparece e a versao antiga nao abre.

## Temas

`themes/themes.txt` e a lista de temas extras que o programa baixa. Uma linha por tema, seis campos separados por barra:

```
nome|titulo|destaque|borda|selecao|arco_iris
```

## O que este repositorio guarda

So o executavel publicado, os temas e esta pagina. O codigo fica em repositorio privado. O programa nao envia token, chave nem dado da maquina para lugar nenhum; a unica consulta de rede e a API publica do GitHub para saber a ultima versao.

## Licenca

MIT. Veja [LICENSE](LICENSE).
