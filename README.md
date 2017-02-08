vital-Vim-Buffer-ANSI
==============================================================================
[![Travis CI](https://img.shields.io/travis/lambdalisue/vital-Vim-Buffer-ANSI/master.svg?style=flat-square&label=Travis%20CI)](https://travis-ci.org/lambdalisue/vital-Vim-Buffer-ANSI)
[![AppVeyor](https://img.shields.io/appveyor/ci/lambdalisue/vital-Vim-Buffer-ANSI/master.svg?style=flat-square&label=AppVeyor)](https://ci.appveyor.com/project/lambdalisue/vital-Vim-Buffer-ANSI/branch/master)
![Version 1.0.0-dev](https://img.shields.io/badge/version-1.0.0--dev-yellow.svg?style=flat-square)
![Support Vim 7.3.429 or above](https://img.shields.io/badge/support-Vim%207.3.429%20or%20above-yellowgreen.svg?style=flat-square)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Doc](https://img.shields.io/badge/doc-%3Ah%20vital--Vim--Buffer--ANSI-orange.svg?style=flat-square)](doc/Vital/Vim/Buffer/ANSI.txt)


Introductions
-------------------------------------------------------------------------------

To visualize ANSI color on Vim buffer.

Install
-------------------------------------------------------------------------------

Install this repository with your favorite Vim plugin manager and then

```vim
:Vitalize . +Vim.Buffer.ANSI
```

To activate Vim.Buffer.ANSI on your plugin.

Usage
-------------------------------------------------------------------------------

```vim
let s:ANSI = vital#vital#import('Vim.Buffer.ANSI')

function! s:demo() abort
  let content = [
        \ "\e[31mRed\e[m",
        \ "\e[32mGreen\e[m",
        \ "\e[33mYellow\e[m",
        \]
  new
  call append(0, content)
  call s:ANSI.define_syntax()
endfunction

call s:demo()
```
