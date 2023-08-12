# docs.development-environment

## What A Section Should Contain

- Header
- Language Versioner
  - What manages the version of the language "versioner" e.g. Brew manages NVM, SDK Man is self updating.
- Language Version
  - What manages the version of language e.g. NVM for NodeJs, SDK Man for Java, etc.
- Install & Build Tool
  - What install/build tool is used per language e.g. gradle for Java, yarn for NodeJs

## Java

| Language Versioner | Language Version | Install & Build Tool |
| ------------------ | ---------------- | -------------------- |
| Self managing      | SDK Man          | gradle               |

### SDK Man

- Install an SDK or Library:

```bash
sdk install java
```

```bash
sdk install gradle
```

- Check the latest version we are using:

```bash
sdk current java
```

```bash
sdk current gradle
```

- Upgrade all versions of the SDKs that are managed and installed by SDK Man:

```bash
sdk upgrade
```

## NodeJs

| Language Versioner | Language Version | Install & Build Tool |
| ------------------ | ---------------- | -------------------- |
| Brew               | NVM              | ryan                 |

### NVM

## Python

| Language Versioner | Language Version | Install & Build Tool |
| ------------------ | ---------------- | -------------------- |
| Brew               | Brew and alias   | pipenv               |
