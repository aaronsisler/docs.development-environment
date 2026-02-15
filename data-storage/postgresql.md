# PostgreSQL

| Versioner | .zshrc Needed | Language Version | Alias Needed | Install & Build Tool |
| --------- | ------------- | ---------------- | ------------ | -------------------- |
| Homebrew  | No            | Homebrew         | No           | N/A                  |

## Homebrew

- List out what versions of software is installed on machine from Homebrew

```bash
brew list postgresql
```

- List out all versions of specific software that are available from Homebrew

```bash
brew search postgresql
```

- List out all versions of PostreSQL that are available from Homebrew for that version

```bash
brew list postgresql@XX
```

- Install a version of PostreSQL

```bash
brew install postresql@XX
```

- Handle possible link issues where the latest installation isn't working alias/PATH wise

```bash
brew unlink postgresql@17
brew link postgresql@18
```
