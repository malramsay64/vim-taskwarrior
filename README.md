vim-taskwarrior
===============

A vim interface for [taskwarrior](http://taskwarrior.org)

The newest version of taskwarrior is always suggested

----

(add this line to .taskrc, or wrapping may be mangled :)

    defaultwidth=999

----

### Default map:

```vim
nnoremap <buffer> A       ...  " add annotation
nnoremap <buffer> D       ...  " delete task
nnoremap <buffer> a       ...  " create new task.
nnoremap <buffer> d       ...  " set the task in current line done.
nnoremap <buffer> f       ...  " change filter
nnoremap <buffer> c       ...  " new command
nnoremap <buffer> m       ...  " modify current field.
nnoremap <buffer> M       ...  " modify current task.
nnoremap <buffer> q       ...  " quit buffer.
nnoremap <buffer> r       ...  " clear all completed task.
nnoremap <buffer> u       ...  " undo last change.
nnoremap <buffer> x       ...  " delete annotation.
nnoremap <buffer> +       ...  " start task
nnoremap <buffer> -       ...  " stop task
nnoremap <buffer> S       ...  " sync with taskd server.
nnoremap <buffer> s       ...  " sort by this column primarily.(if already of the highest priority then switch the polarity)
nnoremap <buffer> <       ...  " sort by this column increasingly.(if already increasingly then increase its priority)
nnoremap <buffer> >       ...  " sort by this column decreasingly.(if already decreasingly then decrease its priority)
nnoremap <buffer> H       ...  " cycle column format left
nnoremap <buffer> L       ...  " cycle column format right
nnoremap <buffer> <F1>    ...  " view the documents
nnoremap <buffer> <CR>    ...  " show task info.
nnoremap <buffer> <TAB>   ...  " jump to the next column
nnoremap <buffer> <S-TAB> ...  " jump to the previous column
nnoremap <buffer> <right> ...  " jump to the next non-empty column
nnoremap <buffer> <left>  ...  " jump to the previous non-empty column

```

### Commands:

```vim
:TW [args]            " task [filter report arguments]
:TWUndo               " undo the previous modification
:TWEditTaskrc         " edit ~/.taskrc
:TWEditVitrc          " edit ~/.vitrc
:TWDeleteCompleted    " clear all completed tasks
:TWAdd                " add new tasks interactively
:TWAnnotate           " add an annotation
:TWComplete           " mark task done
:TWDelete             " deleta a task
:TWDeleteAnnotation   " delete an annotation
:TWModifyInteractive  " make changes to a task interactively (use with caution!)
:TWReportInfo         " run the info report
:TWReportSort         " overide the sort method, reset to default if no arguments passed
:TWSync               " synchronise with taskd server
:TWToggleReadonly     " toggle readonly option
:TWToggleHLField      " toggle highlight field option

```

### Options

```vim
" default task report type
let g:task_report_name     = 'next'
" whether the field under the cursor is highlighted
let g:task_highlight_field = 1
" can not make change to task data when set to 1
let g:task_readonly        = 0
" allows user to override task configurations. Seperated by space. Defaults to ''
let g:task_rc_override     = 'rc.defaultwidth=999'
" default fields to ask when adding a new task
let g:task_default_prompt  = ['due', 'description']
" whether the info window is splited vertically
let g:task_info_vsplit     = 0
" info window size
let g:task_info_size       = 15
" info window position
let g:task_info_position   = 'belowright'
```

### License

[MIT](https://raw.github.com/farseer90718/vim-taskwarrior/master/LICENSE.txt)
