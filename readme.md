# cz-emoji-japanese

> Commitizen adapter formatting commit messages using emojis.

**cz-emoji** allows you to easily use emojis in your commits using [commitizen].

```sh
? Select the type of change you are committing: (Use arrow keys)
❯ feature   🌟  A new feature
  fix       🐞  A bug fix
  docs      📚  Documentation change
  refactor  🎨  A code refactoring change
  chore     🔩  A chore change
```

## Install

**Globally**

```bash
npm install --global cz-emoji-japanese

# set as default adapter for your projects
echo '{ "path": "cz-emoji-japanese" }' > ~/.czrc
```

**Locally**

```bash
npm install --save-dev cz-emoji-japanese
```

Add this to your `package.json`:

```json
"config": {
  "commitizen": {
    "path": "cz-emoji-japanese"
  }
}
```

## Usage

```sh
$ git cz
```

## Customization

By default `cz-emoji` comes ready to run out of the box. Uses may vary, so there are a few configuration options to allow fine tuning for project needs.

### How to

Configuring `cz-emoji` can be handled in the users home directory (`~/.czrc`) for changes to impact all projects or on a per project basis (`package.json`). Simply add the config property as shown below to the existing object in either of the locations with your settings for override.

```json
{
  "config": {
    "cz-emoji-japanese": {}
  }
}
```

### Configuration Options

#### Types

By default `cz-emoji` comes preconfigured with the [Gitmoji](https://gitmoji.carloscuesta.me/) types.

An [Inquirer.js] choices array:

```json
{
  "config": {
    "cz-emoji-japanese": {
      "types": [
        {
          "emoji": "🌟",
          "code": ":star2:",
          "description": "A new feature",
          "name": "feature"
        }
      ]
    }
  }
}
```

#### Scopes

An [Inquirer.js] choices array:

```json
{
  "config": {
    "cz-emoji-japanese": {
      "scopes": ["home", "accounts", "ci"]
    }
  }
}
```

#### Symbol

A boolean value that allows for an using a unicode value rather than the default of [Gitmoji](https://gitmoji.carloscuesta.me/) markup in a commit message. The default for symbol is false.

```json
{
  "config": {
    "cz-emoji-japanese": {
      "symbol": true
    }
  }
}
```

#### Skip Questions

An array of questions you want to skip:

```json
{
  "config": {
    "cz-emoji-japanese": {
      "skipQuestions": ["scope", "issues"]
    }
  }
}
```
