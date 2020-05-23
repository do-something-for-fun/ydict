```text
██╗   ██╗██████╗ ██╗ ██████╗████████╗
╚██╗ ██╔╝██╔══██╗██║██╔════╝╚══██╔══╝
 ╚████╔╝ ██║  ██║██║██║        ██║   
  ╚██╔╝  ██║  ██║██║██║        ██║   
   ██║   ██████╔╝██║╚██████╗   ██║   
   ╚═╝   ╚═════╝ ╚═╝ ╚═════╝   ╚═╝   
 ```

Ydict, another command-line youdao dictionary for geeks!

## Features

* Chinese -> English
* English -> Chinese
* Show hints if word is not found
* Speech
* Show example sentences
* Vim support

## Installation

#### Using Go

```bash
go get github.com/do-something-for-fun/ydict
```

## Speech

Starting from V0.9, speech feature is available. You need to install mpg123 to enable this feature.

___NOTICE:___ Currently, speech feature is only available for MacOS/Linux.

#### Mac OS

```bash
brew install mpg123
```
#### Ubuntu

```bash
sudo apt-get install mpg123
```

#### CentOS

```bash
yum install -y mpg123
```

## Usage

```text
ydict [flags]

Flags:
  -c, --cache       Query with local cache, and save the query word(s) into the cache.
  -d, --delete      Remove word(s) from the cache.
  -h, --help        help for ydict
  -l, --list        List all the words from the local cache.
  -m, --more        Query with more example sentences.
  -p, --play int    Scan and display all the words in local cache.
  -q, --quiet       Query with quiet mode, don't show spinner.
  -r, --reset       Clear all the words from the local cache.
  -s, --sentence    Translation of sentences.
  -v, --voice int   Query with voice speech, the default voice play count is 0.
```

1. Query

```text
ydict <word(s) to query>
```

2. Query with speech (__Available for MacOS & Linux__)

```text
ydict -v 1 <word(s) to query>
```

3. Query and show more example sentences

```text
ydict -m <word(s) to query>
```

4. Query and add this word into local cache, next time when you query the same word, it will be feched from the local cache and be much more faster.

```text
ydict -c <word(s) to query>
```

5. Query sentence

```text
ydict -s "你觉得咋样？"
```

## SOCKS5 proxy

Starting from V0.5, you can use SOCKS5 proxy. At the same directory of ydict, just create a ```.env``` file:

```text
SOCKS5=127.0.0.1:7070
```

Now all the queries will go through the specified SOCKS5 proxy.

## New words notebook

Starting from ydict V2.0, new words notebook is supported. You can use is to add/delete your new words and play it.

* Add a new word to the notebook
```bash
ydict -c hello
```

* Remove a word from the notebook
```bash
ydict -d hello
```

* List all the words from the notebook
```bash
ydict -l
```

* Display a random word from the notebook for every 10 seconds
```bash
ydict -p 10
```

## Help

Just type "ydict" to get help.
  
## Licence

[MIT License](https://github.com/TimothyYe/ydict/blob/master/LICENSE)
