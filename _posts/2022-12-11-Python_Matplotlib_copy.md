---
layout: post
title: "Python - matplotlib-2"
categories: python
author: "aureusoh"
meta: "Springfield"
---

<style>.highlight .hll { background-color: #ffffcc }
.highlight .c { color: #60a0b0; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #007020; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .cm { color: #60a0b0; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #007020 } /* Comment.Preproc */
.highlight .c1 { color: #60a0b0; font-style: italic } /* Comment.Single */
.highlight .cs { color: #60a0b0; background-color: #fff0f0 } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #808080 } /* Generic.Output */
.highlight .gp { color: #c65d09; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0040D0 } /* Generic.Traceback */
.highlight .kc { color: #007020; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #007020; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #007020; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #007020 } /* Keyword.Pseudo */
.highlight .kr { color: #007020; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #902000 } /* Keyword.Type */
.highlight .m { color: #40a070 } /* Literal.Number */
.highlight .s { color: #4070a0 } /* Literal.String */
.highlight .na { color: #4070a0 } /* Name.Attribute */
.highlight .nb { color: #007020 } /* Name.Builtin */
.highlight .nc { color: #0e84b5; font-weight: bold } /* Name.Class */
.highlight .no { color: #60add5 } /* Name.Constant */
.highlight .nd { color: #555555; font-weight: bold } /* Name.Decorator */
.highlight .ni { color: #d55537; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #007020 } /* Name.Exception */
.highlight .nf { color: #06287e } /* Name.Function */
.highlight .nl { color: #002070; font-weight: bold } /* Name.Label */
.highlight .nn { color: #0e84b5; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #062873; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #bb60d5 } /* Name.Variable */
.highlight .ow { color: #007020; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mf { color: #40a070 } /* Literal.Number.Float */
.highlight .mh { color: #40a070 } /* Literal.Number.Hex */
.highlight .mi { color: #40a070 } /* Literal.Number.Integer */
.highlight .mo { color: #40a070 } /* Literal.Number.Oct */
.highlight .sb { color: #4070a0 } /* Literal.String.Backtick */
.highlight .sc { color: #4070a0 } /* Literal.String.Char */
.highlight .sd { color: #4070a0; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #4070a0 } /* Literal.String.Double */
.highlight .se { color: #4070a0; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #4070a0 } /* Literal.String.Heredoc */
.highlight .si { color: #70a0d0; font-style: italic } /* Literal.String.Interpol */
.highlight .sx { color: #c65d09 } /* Literal.String.Other */
.highlight .sr { color: #235388 } /* Literal.String.Regex */
.highlight .s1 { color: #4070a0 } /* Literal.String.Single */
.highlight .ss { color: #517918 } /* Literal.String.Symbol */
.highlight .bp { color: #007020 } /* Name.Builtin.Pseudo */
.highlight .vc { color: #bb60d5 } /* Name.Variable.Class */
.highlight .vg { color: #bb60d5 } /* Name.Variable.Global */
.highlight .vi { color: #bb60d5 } /* Name.Variable.Instance */
.highlight .il { color: #40a070 } /* Literal.Number.Integer.Long */
</style>
<style>
body {
  margin: 0;
  padding: 0;
  font: 15px 'Source Sans Pro', sans-serif;
  line-height: 1.6em;
  color: #222;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
}
a {
  color: #007EE5;
  text-decoration: none;
}
a:hover {
  color: #007EE5;
  text-decoration: none;
}
header.main-header {
  background: none repeat scroll 0% 0% #205F29;
  margin-bottom: 0px;
}
header.main-header a {
  color: #fff;
}
header.main-header .container {
  max-width: 1000px;
}
header.main-header .container nav a:hover {
  background-color: #5C881C;
}
article {
  margin: 0;
}
article header.about {
  margin-bottom: 0px;
  padding-bottom: 0px;
}
article header {
  margin-bottom: 20px;
  padding-bottom: 20px;
}
article header h1 {
  margin-bottom: 2px;
  font-weight: 700;
  color: #000;
}
article header time {
  color: #9E9E9E;
  font-size: 0.85em;
  float: right;
}
article header time.left {
  color: #9E9E9E;
  font-size: 0.85em;
  float: left;
}
article div.social-links ul {
  padding: 0px;
}
article div.social-links li {
  display: inline;
  font-size: 20px;
}
article div.social-links li a {
  color: #000;
  padding: 10px;
}
article div.social-links li a:hover {
  color: #666;
  text-decoration: none;
}
article p {
  font-size: 16px;
  margin-bottom: 20px;
  line-height: 1.6em;
}
article p.note {
  background: #f5f5f5;
  border: 1px solid #ddd;
  padding: 0.533em 0.733em;
}
article p.update {
  background-color: #FEEFB3;
  border: 1px solid #e6e68a;
  padding: 0.533em 0.733em;
}
article p.alert {
  background-color: #ffe2e2;
  border: 1px solid #ffb2b2;
  padding: 0.533em 0.733em;
}
article ul,
article ol {
  margin-top: 0px;
  margin-bottom: 25px;
}
article li {
  font-size: 16px;
  line-height: 1.6em;
}
article a:hover {
  text-decoration: underline;
}
article blockquote {
  border-left: 2px solid #c7c7cc;
  color: #666;
  margin: 30px 0;
  padding: 0 0 0 25px;
}
article img {
  max-width: 100%;
}
article code {
  color: #333;
  background-color: #EEE;
  border-radius: 0;
  font-size: 13px;
}
article .meta {
  font-size: 11px;
}
article .meta a:hover {
  text-decoration: none;
}
article .meta div {
  margin-bottom: 20px;
  display: block;
}
article .meta a.tag {
  margin: 0 10px 10px 0;
  padding: 1px 12px;
  display: inline-block;
  font-size: 14px;
  color: rgba(0, 0, 0, 0.8);
  background: rgba(0, 0, 0, 0.05);
}
article .meta a.tag:hover {
  background: rgba(0, 0, 0, 0.15);
}
article .meta a.read_more,
article .meta a.comments_btn {
  font-size: 14px;
  font-weight: 800;
  padding: 10px 20px;
  color: #205F29;
  background: #FFF;
  border: 1px solid #205F29;
}
article .meta a.read_more:hover,
article .meta a.comments_btn:hover {
  color: #FFF;
  background: #5C881C;
}
.index {
  max-width: 700px;
}
.index article header h2 {
  font-size: 36px;
  margin-bottom: 2px;
  font-weight: 700;
}
.index article header h2 a {
  color: #000;
}
.index article header h2 a:hover {
  color: #007EE5;
  text-decoration: none;
}
.index .separator {
  padding: 40px 0 0 0;
  margin: 0 0 40px 0;
  height: 10px;
  border-bottom: solid 1px #CCC;
}
.index .pagination {
  display: block;
  margin-bottom: 100px;
}
.index .pagination .left {
  text-align: right;
}
.index .pagination .right {
  text-align: left;
}
.index .pagination a {
  display: inline-block;
  border: 2px solid #5C881C;
  margin: 0 5px;
  padding: 8px 20px;
  font-weight: bold;
  color: #5C881C;
}
.index .pagination a:hover {
  color: #FFF;
  background: #5C881C;
}
.post {
  max-width: 700px;
}
.post h2:before {
  content: "# ";
  font-weight: bold;
  color: #DDD;
}
.post h3:before {
  content: "## ";
  font-weight: bold;
  color: #DDD;
}
.post h4:before {
  content: "### ";
  font-weight: bold;
  color: #DDD;
}
.post article .meta {
  margin: 50px 0 100px;
}
.list {
  max-width: 700px;
}
.list ul.double-list {
  margin: 0 auto 60px;
  padding: 0;
  list-style-type: none;
}
.list ul.double-list li {
  padding: 5px 0;
}
.list ul.double-list li h2 {
  font-size: 1em;
  display: inline;
  font-weight: normal;
}
.list ul.double-list li span {
  font-family: sans-serif;
  text-transform: uppercase;
  text-align: right;
  float: right;
  padding-top: 3px;
  font-size: 12px;
  color: #999;
}
.full-width-content {
  padding-top: 10px;
  padding-left: 0px;
  padding-right: 0px;
  margin-left: -20px;
  margin-right: -20px;
}
.col-xs-1,
.col-sm-1,
.col-md-1,
.col-lg-1,
.col-xs-2,
.col-sm-2,
.col-md-2,
.col-lg-2,
.col-xs-3,
.col-sm-3,
.col-md-3,
.col-lg-3,
.col-xs-4,
.col-sm-4,
.col-md-4,
.col-lg-4,
.col-xs-5,
.col-sm-5,
.col-md-5,
.col-lg-5,
.col-xs-6,
.col-sm-6,
.col-md-6,
.col-lg-6,
.col-xs-7,
.col-sm-7,
.col-md-7,
.col-lg-7,
.col-xs-8,
.col-sm-8,
.col-md-8,
.col-lg-8,
.col-xs-9,
.col-sm-9,
.col-md-9,
.col-lg-9,
.col-xs-10,
.col-sm-10,
.col-md-10,
.col-lg-10,
.col-xs-11,
.col-sm-11,
.col-md-11,
.col-lg-11,
.col-xs-12,
.col-sm-12,
.col-md-12,
.col-lg-12 {
  padding-right: 0px;
  padding-left: 0px;
}
</style>

<style type="text/css">/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}

div.my_inner_cell {
  flex: 1;
}

/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area 
div.output_area 
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}



.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}






.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}








.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}


.rendered_html pre,



.rendered_html tr,
.rendered_html th,

.rendered_html td,


.rendered_html * + table {
  margin-top: 1em;
}

.rendered_html * + p {
  margin-top: 1em;
}

.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,

.rendered_html img.unconfined,

div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered 
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
</style>
<style type="text/css">.highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */</style>
<style type="text/css">
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }
</style>

2


# Python matplotlib

## 1. 개요

MATLAB은 simulink도 압도적인 역할을 하지만, graph 기능 또한 탁월합니다. 마치 Photoshop을 그림 배경 지우는 용도로만 사용하시는 분들이 있듯이, MATLAB을 graph 그리는 분들도 더러있습니다. 그러나, 단순히 graph를 그리는 용도로만 MATLAB을 쓰기에는 너무나도 비쌉니다.
matplotlib를 이용하면 MATLAB과 유사하게 graph를 그릴 수 있습니다. Excel의 graph로는 부족하신분들, 데이터 분석하시는분들에게 필수적인 라이브러리입니다.

! matplotlib에서 사용하는 기본 자료형은 numpy를 이용합니다. 아직 numpy가 익숙하지 않으신 분들은 numpy를 보신 후 다시 보시기를 권장합니다.

## 2. Graph

1.
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>

2.
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>
</div>

3.
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>
</div>

4.
<div class="jp-Cell-inputWrapper">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span></pre></div>
</div>
</div>

4-1.
<div class="jp-Cell-inputWrapper">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span>It's</span> <span>real test.</span></pre></div>
</div>
</div>

4-2.
<div class="jp-Cell-inputWrapper">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><span>It's</span> <span>real test.</span></div>
</div>
</div>

4-3.
<div class="jp-Cell-inputWrapper">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre>It's real test.</pre></div>
</div>
</div>

5.
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>
</div>
</div>
</div>

10.
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Plotting-from-a-script">Plotting from a script<a class="anchor-link" href="#Plotting-from-a-script">&#182;</a></h4><p>If you are using Matplotlib from within a script, the function <code>plt.show()</code> is your friend.
<code>plt.show()</code> starts an event loop, looks for all currently active figure objects, and opens one or more interactive windows that display your figure or figures.</p>
<p>So, for example, you may have a file called <em>myplot.py</em> containing the following:</p>
<div class="highlight"><pre><span></span><span class="c1"># ------- file: myplot.py ------</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="kn">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="kn">as</span> <span class="nn">np</span>

<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
<p>You can then run this script from the command-line prompt, which will result in a window opening with your figure displayed:</p>

<pre><code>$ python myplot.py</code></pre>
<p>The <code>plt.show()</code> command does a lot under the hood, as it must interact with your system's interactive graphical backend.
The details of this operation can vary greatly from system to system and even installation to installation, but matplotlib does its best to hide all these details from you.</p>
<p>One thing to be aware of: the <code>plt.show()</code> command should be used <em>only once</em> per Python session, and is most often seen at the very end of the script.
Multiple <code>show()</code> commands can lead to unpredictable backend-dependent behavior, and should mostly be avoided.</p>

</div>
</div>
</div>

6.
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>
</div>
</div>
</div>

7.
<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>

</div>
</div>
</div>
</div>

</div>

8.

<div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[18]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[&lt;matplotlib.lines.Line2D at 0x7ff629af5100&gt;]</pre>
</div>

</div>

<div class="jp-OutputArea-child">
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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"
class="
"
>
</div>

</div>

</div>

</div>

</div>

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>After running this command (it needs to be done only once per kernel/session), any cell within the notebook that creates a plot will embed a PNG image of the resulting graphic:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>

<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">),</span> <span class="s1">&#39;-&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">x</span><span class="p">),</span> <span class="s1">&#39;--&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAX8AAAEACAYAAABbMHZzAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAIABJREFUeJzt3Xd4FVX+x/H3SSH0Jr33YqQjgiBFitQkdBQUZV1Zy6qr
rt0FXVfF9lvFBq4FkKa00ERAiNJBiiGUhN4UQgsQIKSd3x8nKCIh5c6dMzP3vJ6HR5LcO/MxTL45
c+YUIaXEMAzDCCxBugMYhmEY9jPF3zAMIwCZ4m8YhhGATPE3DMMIQKb4G4ZhBCBT/A3DMAKQJcVf
CPGZEOKYECL2Oq95XwixSwixRQjR1IrzGoZhGPljVcv/C+CO7L4ohOgB1JZS1gVGAp9YdF7DMAwj
Hywp/lLKlcDp67wkEpiY9dp1QAkhRHkrzm0YhmHknV19/pWBQ1d8fCTrc4ZhGIYG5oGvYRhGAAqx
6TxHgKpXfFwl63N/IoQwiw0ZhmHkkZRS5OX1Vrb8Rdafa5kL3AMghGgNJEkpj2V3ICklUkpOXTjF
v5b9i63Htv72Oaf9OX5c0r+/5MYbJfPmSVJTr//6hARJv36SBg0kq1Zd/7WjRo3S/v/nhD/m++D9
70VGhmTMGEnZspKXXpIcPnz9158/L2nffhSlS0v+/W/JxYv6/x90/skPq4Z6TgFWA/WEEAeFEPcJ
IUYKIR7IKuYLgX1CiN3AOOCh3By3VKFSvNzpZW4qd5MVMS03fz40bgw1a8LGjdC7N4SGXv89devC
zJnw739D//7wj39Aero9eQ0D4KEFDzEvfp7uGL85eRIiImDOHPjpJ3jlFaicwxPBwoWhUyf1c7dp
E7RuDb/+ak9er7BqtM9dUspKUsowKWU1KeUXUspxUsrxV7zmESllHSllEynlJivOq9Nnn8GDD8L0
6fDWW1CwYN7eP2AAxMXBtm0wdCikpfknp+EdmTKTH/b/wL7T+3w6zrDGw3ho4UO8uOzFfLcarbJ1
KzRvDg0awA8/QLVqeXt/jRqqMTVwILRrB7t3+yWmJ7nyga+Ukv1J+7Wd/4svYPRoWL4cbrst/8e5
4QaYOxeSk2HIEEhN/ePXO3bs6EtMzzDfB0jNSGX4nOEklk2keFhxn451a9Vb2fTAJr7d/S2jYkZZ
lDDvdu+G7t3htdfg7bdzvmu+2uXrQgh44QV45hlo3x42b7Y+qyfp7qu6Rt+VzEncsThZ7q1ycnvi
9hxfa7Uvv5SycmUp4+OtO2ZKipSRkVL26aP+bhhXyszMlMNmDZO9JveS51PPW3bcY8nHZL2x9eR7
a9+z7Ji5dfiwlDVrSvnJJ9Yed+ZMKcuWlTIuztrjOl1W3cxTrXVlyz+8XDhjuoyh15ReHEvO9rmx
5ebMgeefh6VLoV49644bFgbffAPBwfBQrp6GGIHk7dVvs/34dr4e+DWFQwtbdtxyRcqxeNhiNv66
kUyZadlxc3LyJHTrBg88ACNHWnvsfv3UXURUFJw6Ze2xvUZIzX1+VxNCyNxmGrV8FIv2LGL58OWW
/lBcy5490KYNLFgAN9/sn3MkJ0OrVvDkk/CXv/jnHIa7JJxMoNOETqz9y1qqlqia8xscLiMDOndW
P0Nvvqm6bPzhiSfUM7WFCyHErgHtGgkhkHkc6unq4i+lZPic4WTIDCb3m+y3TCkp0LYt3Hsv/P3v
fjsNADt2qH7LxYuhWTP/nstwh1MXT1G6UGndMSzx6qvqWdmSJRDkx36H9HTo0QOaNFF3Al6Xn+Lv
ym6fy4QQjOs9DoEgOTXZb+d54gmoVQseecRvp/hNw4bwwQdqNNDp662WZAQMrxT+NWvUtT1xon8L
P6jW/vTpqqv266/9ey63cnXL3w7Tp6uRBBs3QokS9p338cfh4EGYNcu+cxqGv5w5A02bwn//C5GR
9p13/Xo1h2DrVihb1r7z2i3gWv7+lpiounmmT7e38AOMGQPbt8Ps2fae1whsUkoip0WScDLB0uM+
+KDqhrGz8IN6hjZsGDz2mL3ndQNT/K/j6afVhdOihf3nDguDcePg0Ufh7Fn7z2/okZqRyqZf9c2B
FELQpWYXRkSPsGwC2Pz56s5ZV9/7K6+oO4B5zpnU7Aim+Gfjhx/g++/h5Zf1ZejQAbp2hZde0pfB
sNfrK17n5R80XnTAQzc/REp6CpO3+j6IIiVFtbrHjlVLMuhQuDB8+qm6+zhzRk8GJ/Jcn//x88eZ
nzCf+5rdl+9jpKaq/snL6+/odPIkhIerVou/hpgazrDj+A7af9meLSO3ULm43u0u1hxaw4BvBrDz
4Z0UCyuW7+O8+qpae8cJz65GjlRDSz/x4D6CATfU81rOpJyh/gf1WTRsEU0r5G+r4DfegBUr1O2q
v8Yh58WkSfDuu7BhQ2CMWQ5UEVMj6FijI0+0eUJ3FACGzxlOhSIVGNN1TL7ef+CAWrdn40a1Bo9u
SUlQv76apNmoke401jIPfIESBUswuuNoHl/0eL76LA8fVn2TY8c6o/CDeu5QrJj6JWB4U8z+GLYm
buXhmx/WHeU3Y7qMoXbp2vl+/1NPqS4fJxR+gJIl1Qz9Z57RncQZPNfyB0jPTKfZuGa80vEV+jbs
m6f3jhwJpUqp1r+TrF6tFn9LSMj7CqKG83Wd1JURTUdwZ6M7dUexxLJlcP/9atXaQoV0p/ldaqqa
SzN+vJpp7BWm2+cKS/Ys4W8L/sb2h7YTFhKWq/fs3q3WBU9IgNIOnFcTGQkdO6o9AAxvOX3xNCUK
liBIuP9mXEr1c/TkkzBokO40f/b112oo9YYN/p9sZhfT7XOFrrW70rRCU1YeXJnr94wapSZXObHw
A/znP+qOxAz99J5ShUp5ovCDWk/n4kU1S92JBg5UiyhOm6Y7iV6ebfmDmrAictlxHxurVhrctUv1
rzvV8OGqD1XnEFTDyI6U0LIlvPgi9M1bj6utfvhB/SzFx6s5NW5nWv5XyW3hBzWW/plnnF34QRX9
Dz5Qs48Nwy4ZmRnM2Tknx0EU0dHqF0BUlE3B8qlDB7jxRvjyS91J9PF08c+tdevUWOQHH9SdJGc1
aqhtH998U3cSI9A8//3zLN6zONuvZ2aqrtOXX3bOSLnreeEF9XMUqHtom+KPmojy/PPuGUXzz3+q
rSTNqp/ulZaRRt/pfTl36ZzuKLkSHBTMqA6jGBUzKtvW/6xZUKAA9O5tc7h8atsWqlQJ3FU/A6r4
X+ui3b5dPfW/91778+RX1arqB+zjj3UnMfJrytYpnL101qfZs3YbGD6Q5NRkFu1e9KevSanW0HFL
q/+y55+H119Xdy2BJmCK/+iY0Xyx5Ys/ff7tt9U6/U4ai5wbTz8N77+vRlUY7pKRmcHrK1/n+XbP
646SJ0EiiOfaPcdbq9/609cWL1ZFv0cPDcF80K2buluZP193EvsFTPHvVKMTb6x84w97lR45opZM
dkNf/9XCw9VaPxMm6E5i5NXsnbMpWbAkt9e8XXeUPBsUPohdp3bx89Gf//D5d95Rmx65qdUPKu/z
z6th1A4b+Oh3AVP821dvT7GwYny769vfPvfee3DPPXDDDRqD+eCZZ9SdS0aG7iRGbkkpeW3Fazx/
2/N5Go3mFKHBofxw7w80Kv/74jixsWom750unZzct6+aO7Nsme4k9gqY4i+E4PFbHue/6/4LqKVd
P/vM3bNl27WD8uVh5kzdSYzcOpp8lHJFytG7nkueil5DrVK1/jAh7d13VddpgQIaQ/kgKEgNonj3
Xd1J7OXpSV5Xu5R+iRrv1WDJ3Uv4dsJNbN4MU6b45VS2mTtXPWjbsMF9t9yG+/3yi+qC3LPHuTPj
c+PiRaheHVatgrp1dafJOzPJKwdhIWE82/ZZdibu4v331aqDbte7t1qqdt063UmMQPTBB2reiZsL
P6gBH3/5C3z4oe4k9gmolv9ls2apW7yVuV/2x9HeeQe2bDFLPhv2On9eTTpcswbq1NGdxncHD0Kz
ZmofgqJFdafJG9Pyz6WPPoKHHtKdwjr33aeGqpklHww7TZqcTsWIj6hV2xuD5KtVU6vmTpyoO4k9
Aq74x8fD1q36t2e0UunSasTCZ5/pTmIEkk/HB5PcYBzL9y3XHcUyf/+76spyWIeIXwRc8f/kE9W3
54WV/K708MPq/80M+3QeKSX9pvfj4JmDuqNY5qef4NRJwZMdRjJu4zjdcSzToYNa7vn773Un8b+A
Kv7nz6tbupEjdSexXosWULEiLFigO4lxtVWHVrHt+DaqFK+iO4plPvlE/RwNazyUJXuXcDT5qO5I
lhBCtf7HjtWdxP8CqvhPm6YWc6peXX3c/avu7Du9T28oCz38cGCNVnCLTzd9ysgWIz2zWUtSkppb
ct99as/sAQ0H8MXmPy+d4lZDh8KKFWoFAC/zxtWYC1Kqwnjlg94GZRrw2WbvdJQPHAibN6sNaQxn
SEpJInpnNHc3vlt3FMt89ZVaE6d8efXxyJYjGb9p/B+WTnGzIkXU9pNeX+s/YIr/hg1qVm+3br9/
7q/N/8oXW74gPdMbC3oXLKiWq/j8c91JjMumbp1K19pdKVukrO4olpBSdfn87W+/f65lpZZED4lG
4J1ZhvffrwZQeHm1z4Ap/p9/DiNG/HHD5vBy4dQoWYMFCd7pKL/vPrXYW6BuUOE0a4+s5f5m9+uO
YZnVqyEtTQ2JvFLj8o1duVZRdlq0ULv6xcToTuI/AVH8L15UGzbcc8+fv/bX5n/l002f2h/KT8LD
1XjlxdlvuGTYaELUBLrV7pbzC11i/Hh44AHvLyUihBoV+L//6U7iPwFR/GfPVssfV636568NCh/E
8QvHSUlPsT+Yn4wYYbp+nMQrLeJz59QevXd75/HFdQ0bBgsXenfHvIAo/l98obpDrqVwaGHW3b+O
giEu2cMxFwYPhqVL4fhx3UkML5kxQ42DL1dOdxJ7lC6tNqeZPFl3Ev/wfPE/eFBtzh4VpTuJfUqU
gD59vHvRGnpMmADDh1//NXtO7WF/0n5b8tjhctePF2f8er74T5igWsJu2ZzdKpe7frx40Rr227dP
bdiS0+bsU7ZO4a1Vf97m0a1uv12NEty0SXcS63m6+GdmqrG62XX5eFmHDpCc7M2L1ukOnz3Mqz++
qjuGpSZOhCFDct6w5e4mdzN923QupV+yJ5ifBQWpux0vLvbm6eK/YoVap7tlS91J7BcUpH7pmQe/
9puydYqn1vHJzFR30Pfem/Nra5SsQaPyjZif4J0d0YcOVasDpKXpTmItTxf/y63+3A62mLJ1Cov3
eGeM5LBhaoir1y5aJ5NSMil2kqdm9K5cCYULQ/PmuXv98CbDmfDzBP+GslHdulCzphpE4SWeLf4X
L8KcOXDXXbl/T1pGGh+s/8B/oWxWsybUqwfffac7SeCIPRbLuUvnaFutre4olvnyS9Xqz20jqn/D
/vx44EcSz3tng4m771bLWniJZ4v/ggW/r3SZW/0a9uPHAz9y/Lx3xkgOHWpG/dhpUuwkhjUe5plF
3C5cUPNkhg7N/XuKhRXj0z6femq5h0GDVE05d053Eut44wq9hsmT89bqB3XR9qnfh2lx0/wTSoNB
g9REFS9dtE6VKTOZFjeNYY2H6Y5imfnz1QTJvDSiAAaGD/TMekYAZcvCbbepX4ReYUnxF0J0F0Ls
FEIkCCGeucbXOwghkoQQm7L+vGjFebNz+jQsW5a/3bruaXwPE2O982i/TBl10c6ZozuJ9wWJINb/
dT0NyjTQHcUyU6fCnXfqTuEMw4Z5q+vH5+IvhAgCPgDuAMKBO4UQ17r6f5RSNs/649dxcLNmQZcu
arJTXt1e83YOnz3sqXX+TdePfSoVq6Q7gmWSklQjqm9f3UmcISJCrQ78yy+6k1jDipZ/K2CXlPKA
lDINmAZEXuN1tnUATp6ctz7KKwUHBRP7t1hqlqppbSiNIiJg7Vo4dkx3EsNNZs2Czp2hZEndSZyh
UCH1i3DqVN1JrGFF8a8MHLri48NZn7taGyHEFiHEAiHEjRac95qOHIEtW6Bnz/wfw0t9laA2p+jT
B6ZP153EcBMrunyklKRmpFoTyAGGDoUpU3SnsEaITefZCFSTUl4QQvQA5gD1snvx6NGjf/t7x44d
6Xj14uHXMW2a+u0caMs55GToUBg1Ch59VHcSww2OHlVdHHPn+nact1e/zYkLJxjTdYw1wTTr0AEO
H4bdu6FOHX05YmJiiPFxswEhfVz8RQjRGhgtpeye9fGzgJRSZvuvLYTYB7SQUp66xtekL5latIA3
31S3q8bv0tOhcmVYswZq1dKdxlvOXTpHXGIcbaq20R3FMmPHquLv67IGscdi6TO1D/se2+eZ4a8P
PwyVKsELL+hO8jshBFLKPHWtW/GvsQGoI4SoLoQoAAwB/tBeEEKUv+LvrVC/dP5U+H2VkKAexuTh
RiFghIRAv37wzTe6k3hPdHw0r618TXcMS02ZYs0on0blGlG0QFHWHFrj+8EcYvBgNXPe7Xwu/lLK
DOARYDGwDZgmpdwhhBgphHgg62UDhBBxQojNwH+Bwb6e91q++UYN7wwOtuZ4249v50DSAWsO5gCD
BnnjonWa6dumMzjcL5e0Fvv2qW6NLl18P5YQgjtvupOpcR55Sgq0awcnTsDOnbqT+Mbnbh+r+dLt
07QpvP8+tG9vTZZ/Lf8X51PP884d71hzQM0yMlTXz8qVevsrveT0xdNU/291Dj9xmOJhxXXHscSY
MeoXwCefWHO8Paf20OazNvzy5C+EBNn1mNG/Hn8cSpVSz9GcQFe3jyMkJKihjG0tXFJlyE1DmL5t
Opky07qDahQcrO6MTNePdebsnEPnWp09U/hBXR+DBll3vNqla9O1dld+OeeRAfKo78/06e7eL8Mz
xf+bb2DAAOu6fABuLHsjpQuVZtXBVdYdVDPT9WMtL3b5HDxo3d3zZZP7TaZaiWrWHlSj1q3Vfhlx
cbqT5J+niv/AgdYfd+CNA5mxfYb1B9akXTs1jC8hQXcSb4isH0nvejlsb+UiM2aoodIh3uid8Zug
IPc3pDxR/BMSIDHR2i6fywbcOICZO2Z6qutnwADT9WOVB29+kKIFiuqOYRl/NaK8aPBgd3f9eKL4
Wz3K50oNyzbk+due99QsRbe3WAz/OHBAdfuYodK507Klmj8TG6s7Sf54ovh//bW1D6iu9tDND1Ew
xDtThtu2VUPV4uN1JzGcZMYMiIoyXT65JYSaOzNzpu4k+eP64h8fD8eP+6fLx6uCgsyoH+PP7Ojy
+WjDR2w4ssG/J7FR//6m+Gszc6b6Bwhy/f+Jvfr189bGFHZz2vwYXx08qCZ2derk3/OcuniKr2K9
syj+Lbeopa/dOOHL9SVz1qz8bdoS6G67DQ4dgv37dSdxn7OXzlL/g/qkZaTpjmKZmTMhMhJCQ/17
ngE3DmDGjhmeGUARFOTerh9XF/8DB1SLpV07e84npfRMiy84WP2wz5qlO4n7LEhYQJ3SdQgN9nOl
tNGMGWoUmL81KNOA0oVKe2qtn/793flz5OriP3u22qjErgdUXSZ1IfaYSx/tX0O/fu68aHWbuWMm
/Rt653bz119h+3b7VsLt16Afs3d6p8+xXTt1F73PZZv/ubr4z5pl7xZzzSs099SEr9tvh23b1A+/
kTsX0i6wZO8SIhtca7M6d4qOVpsfFShgz/n6NuzLrB2zPHMXHRLizrto1xb/Y8fU+Fo71+3v17Af
s3a67F/4OsLC1A99dLTuJO6xaPciWlZqSZnCZXRHsczs2fY2opqUb8LSe5YihG07u/qdG0f9uLb4
R0dDjx727th1S5VbOH3xNAknvbM2glv7K3XZcXyHp9bySUpSG/x0727fOYUQ1CrlrR2Fbr9djfg5
ckR3ktxzbfGfNUv1WdspSAQRWT+SOTvn2HtiP7rjDli3Dk5ZvrWON73Q/gUeaPFAzi90ifnz1fDO
ot5ZoUKLAgWgd293DZ92ZfFPSoLVq1XL3279GvYj/oR3psYWKaK6zubN053E0MHuLh8v69vXXV2o
rtzM5auv1GxEN32jneyrr9QSGb5u1m24y4ULULEi7N0LN9ygO437nT+vvp8HDqiNXuwUMJu56Ojy
8bJevSAmRl28RuBYvBhatNBX+KWUbD++Xc/J/aBIEdWFtnCh7iS547rif+ECLF2q+tcMa5QqBa1a
qWJgBI7Zs/U2olIzUmn7eVuOJh/VF8JiUVEwxyWPBF1X/Jcu1dta8aqoKNONdj1zds5h5wkXLuCS
jbQ09bA3KkpfhrCQMHrU6UH0Tu9ceL17q0ZUSoruJDlzXfGPjlYTKgxrRUSoYpCerjuJMz33/XOc
vXRWdwzL/Pgj1KoFVarozdG3QV9PzfYtWxaaNoXvv9edJGeuKv4ZGWpUihOK/6/nfmXizxN1x7BM
tWpQvTqs8s52xZbZeWInZy+dpWWllrqjWMYpjajudbqz+tBqT/1i7dvXHV0/rir+a9aop+k1a+pO
AiFBITz67aOkpLvg/i6XIiPdcdHaLXpnNJH1IwkSrvpxyZaUzin+xcKK0bZaWxbtXqQ7imUiI9XI
uYwM3Umuz1VXs1MuWICyRcrSuHxjlu9brjuKZS73+zts9K92c+LnENVAY+e4xX7+Wa3qetNNupMo
D7Z8kCKhRXTHsEzNmqqRunat7iTX55riL6Vqlep8QHW1iPoRRMd752FVo0bq+7x1q+4kzvHruV+J
PxFPxxoddUexzOVGlFOW1omoH0Gver10x7CUG0b9uKb479gBly5Bs2a6k/wusn4k8xLmeWZjCiHc
cdHaqWiBoswaPIsCwTYteWkDJ91Be1VUlBpK6+S7aNcU/+hoNSLFKa0VgLo31KV4WHE2/rJRdxTL
REaaIZ9XKhZWzFOt/kOH7N0AKVA1aQKpqc7e3tE1xd9pXT6XfRbxGTVK1tAdwzLt2v2+Q5rhPXPn
qmW87doAKVAJoRqrTl4yxRXF/5dfICEBOnTQneTPbq16K2WLlNUdwzIhIao4zJ+vO4nhD6bLxz4R
Ec6+i3ZF8Z8/X63g6e/NpQ3F6S0WI3/OnFEjUO64Q3eSa5u1YxYfbfhIdwzLdOigtsc8dkx3kmtz
RfGfO1cVJMMed9yhJnud9c68mzzLlJmkZaTpjmGpb7+F225z7tr9pQuV5rPNn+mOYZmwMPWztGCB
7iTX5vjif/68mopu505Dga5YMWjbNrAXeltzaA2dJnTSHcNSTm9EtavWjv1J+zl05pDuKJZx8l20
44v/0qVw881QsqTuJNfntZaiky9aO8yNn0unGt4p/mlpsGgR9OmjO0n2QoJC6Fm3J/MTvPPAqUcP
WL4cLl7UneTPHF/8nd5auWz4nOF8ve1r3TEs06ePWpc8UBd6i46PJrKBd56MrlwJtWtDpUq6k1xf
n3p9mJfgnW3lSpeG5s2dudCbo4t/ZqZ62Ovk1splHap38NRFW7WqWuxt9WrdSewXfyKec6nnaF6x
ue4olpk3zx0/R3fUvoNVh1ZxMc2BTeV8cupdtKOL//r1aonUWrV0J8lZr7q9+G7Pd57r+gnEvX3n
JcyjT70+nlrIzS130CUKlmD/Y/spFFpIdxTLXP45ynTYQgCOvrrdcsECVCxWkbql67Li4ArdUSzj
1BaLv528cJJ+Db2zT+jOnWq2aZMmupPkTqlCNm+A62e1a6vunw0bdCf5I1P8LRRRP4J58d5pKjdr
pkZbxcfrTmKv17u8Trfa3XTHsMzcuarLx0lLowSaPn2cdxft2OK/dy+cOKH2lnWLiPoRnLx4UncM
ywihLlonz1I0cuaW/n4vc2LxF9Jhy84JIaSUkvfeU0sL/+9/uhMFtoUL4fXXYYV3erMCyvHjUKcO
JCaqSUeGHhkZUKEC/PST2jHPakIIpJR5urdzbMt/7ly1GbKh1+23q80/TnrnhiagLFwIXbq4r/Bn
ykzWHnb4bih5EBzsvDWzHFn8z5xRI326dtWdxChYUP0CWLhQdxIjP9zc5RM1LYq9p/fqjmGZPn2c
NYDCkcX/u+/UGiRFvLOzm6s5sb/SH6ZsncL249t1x7DMpUtqhnwvF26SFSSC6FW3l6cGUHTrpubN
nDunO4niyOLv5taKF/Xqpdb5SU3VncR/pJS8tPwlT83TiImB8HA1V8aN+tT31mzf4sXh1luds2aW
I4v/t9+6u7//8NnDjN84XncMy1SoAPXrqwX2vGrHiR2kZaTRuHxj3VEsM2+eu3+Outbqyvoj6zmT
ckZ3FMs46S7akcW/alX1x63CgsN4esnTXEq/pDuKZZx00frDvHg1q1d4ZDC8lO5ZGiU7RQoUoV21
dny35zvdUSxzec2sjAzdSRxa/N18wQKULVKW8HLhxOyP0R3FMpeLv8NGBltmbsJc+tR3+YV3hbg4
NU8jPFx3Et88fPPDlC5UWncMy1Svru6k163TncSi4i+E6C6E2CmESBBCPJPNa94XQuwSQmwRQjS9
3vHcXvzBe6sTNm6sVvjcsUN3EusdP3+cuMQ4T23Ufvm5mdtvZHrV60WXWl10x7CUU+6ifS7+Qogg
4APgDiAcuFMI0eCq1/QAaksp6wIjgU+ud8wWLXxNpV/ver2ZnzAfp02iy6/Ls32dcNFarUiBIiy4
awEFQwrqjmIZM2jCuZzyc2RFy78VsEtKeUBKmQZMA65eCD0SmAggpVwHlBBClM82lCM7o/ImvGw4
QgjiEuN0R7GMUy5aqxUOLUy7au10x7BMYqK6Q+vQQXcS41patVIzr/ft05vDijJbGbhy37XDWZ+7
3muOXOM1niKEYGr/qVQt4eIn11fp1EktuXHihO4kxvUsWKAmSBYooDuJcS1BQWr4tO6GVIje01/b
6NGjf/t7x44d6dixo7YsvmhdpbXuCJYKC4POndVohXvu0Z3GyM68eRAVpTuFcT19+sBHH8Gjj+bv
/TExMcTExPiUweeF3YQQrYHRUsruWR8/C0gp5ZgrXvMJsFxKOT3r451ABynlsWscT3qln9yLvvhC
Ff9vvtGdxLiWS5egXDnYswfKlNGdxjpfbvmSTJnJiGYjdEexRHIyVKwIR46oyV++0rWw2wagjhCi
uhCiADAJnS8DAAAc+klEQVQEuHoFi7nAPVkhWwNJ1yr8hvP16gVLlnhjtq+UkgtpF3THsFRMDNx0
k7cKP0CpgqWYvHWy7hiWKVoU2rbVO9vX5+IvpcwAHgEWA9uAaVLKHUKIkUKIB7JesxDYJ4TYDYwD
HvL1vIYe5cpBw4bwww+6k/hu+/HttBjvgaFlV5g3z10bIOVWl1pd2HBkg5ntayFLxtVIKRdJKetL
KetKKd/I+tw4KeX4K17ziJSyjpSyiZRykxXndYu0jDTSM9N1x7CM7ovWKvMS5tG5ZmfdMSxzea9e
Lw7xLFKgCLdVv41FuxfpjmKZ3r31zvb1wKBK5+s9tTdL9y7VHcMyXpnte3mjdq+IjYXQUHVn5kVe
mzhZvTpUqgRrNW1bYIq/DTrV6OSppWlvukkV/m3bdCfJv+Pnj7MtcZuZ1esiveupRlSmzNQdxTI6
76JN8bdBRP0I5iXMM7N9HWThroV0rtWZsBCXbXF1HV6f1VuleBUS/p5AkPBO2TLF3+MalmlIaHAo
scdidUexjNuL/8mLJxl04yDdMSxz9CgkJKhNkLyseJgF4yId5Oab1RapezVsWGaKvw2EEJ7rr+zQ
QXX7JCbqTpI/T7R5gsE3DdYdwzILFqidosysXnfROdvXFH+b9G3Ql6SUJN0xLBMWppYQMHv7OoPX
u3y8LCJCT/H3eYav1cwMX/eYMEENLZw5U3eSwJaSAuXLq66DG27QncbIq/Pn1WzfQ4egRIn8HUPX
DF8jQPXsqTYIT0nRnSSwLVsGTZoETuFPy0hj9aHVumNYpkgRaN8eFtk8hcEUfyPfypaFRo3UkgKG
PoHW5ZOWmUb3r7pz+uJp3VEso2MAhSn+hk8iIlTXj1vM3D6T9UfW645hGSm9u6RDdgqHFqZjjY4s
3OWdB069e8O336rd8uxiir/hE7fN9h2zagzJqcm6Y1hm82bVbVC/vu4k9ro8d8YrKleGmjVh1Sr7
zmmKv83iT8Tz5ZYvdcewTIMGULAgbNmiO0nOfj33K7tO7eK2at4ZDD93bmC1+i/rXa833+35jtQM
Dywvm8Xurh9T/G0mhOCFZS94Zoq6m2b7zk+YT/c63QkNDtUdxTKBWvwrFK1A/Rvqs+LACt1RLGN3
F6op/jard0M9ihUoxsZfNuqOYhm39Pt7bSG3Q4fg4EFo00Z3Ej2ebvs0RQsU1R3DMk2bwsWLEB9v
z/lM8dcgsn4kc+NdUC1zqW1bNcb8yBHdSbJ3PvU8Mftj6FGnh+4olpk3T80ODXHkZqz+169hP26p
covuGJa5fBdtV0PKFH8NIupHEB0frTuGZUJDoUcPmD9fd5LsFQguwKJhiyhVqJTuKJYJ1C4fL4uI
gGibSoMp/hq0rtKao8lH2Xd6n+4olrHzos2P0OBQbq16q+4Yljl7FlavVuv5GN7RqRPExdmzZpYp
/hoEBwUz/675lCtSTncUy3TvDitXqo2pDf9bvFh1txUrpjuJYaWwMPUL3Y67aFP8NWlVuRVFChTR
HcMyJUpA69bw3Xe6kwQG0+XjXZGR9vT7m+JvWCYqCubM0Z3C+9LT1WqqvXvrTuIMY9eNZdLPk3TH
sEyPHrB8OVy44N/zmOJvWCYiQhWltDTdSf7oTMoZ3REstWoV1KgBVavqTuIM5YqUY2rcVN0xLFO6
NLRooRZN9CdT/A3LVKmipqivXKk7ye/iT8TT5JMmntlCE9TdVWSk7hTO0aNuD1YeXMm5S+d0R7FM
ZKT/B1CY4q/ZhbQLpGU4rKnsAzsu2ryIjo+mR50eCI/sai6lKv5RUbqTOEfxsOK0rdaW7/Z454FT
RIR66JuR4b9zmOKvWa8pvVi2b5nuGJa5XPyd0tCOjo8msoF3msmxsWrrv5tu0p3EWaLqRzFnp3ce
ONWsqTboWbfOf+cwxV+znnV6euqibdRI/TfWAXvVJ55PZFviNjrV6KQ7imUut/o9ciNjmYj6EcTs
j/HMmlng/7toU/w1i2oQRXR8tGcuWiGc0/UzN34ud9S5g7CQMN1RLGO6fK6tYrGK7Hl0D0HCOyUt
MlL9e/vrLto73ymXqntDXUoVKuWpDUaiopxR/C+kXWBoo6G6Y1jmwAE4fBhu9c5EZUt56Zc8qBE/
Fy/Cjh3+Ob4p/g7Qt0FfT3X9tGunCtXBg3pzPHrLo0TU985MqOhotfBXcLDuJIYdhFANqdmz/XN8
U/wdoH/D/qRn2rh/m5+FhKgiZSZ8Wct0+QSevn39V/yF08Y/CyGk0zIZeTd3Lrz7rtnc3SonT0Kt
WnD0KBQqpDuNYZf0dKhYETZuhGrVsn+dEAIpZZ6GAZiWv+EXXbuq/WWPH9edxBsWLIDbbzeFPyfp
menMT3Dw2uJ5FBKilvHwx120Kf6GXxQqBHfc4Y4dvtxg1izo1093CucLEkE8MO8BEk4m6I5iGX91
/Zjib/iNP/srr+f9de/z89Gf7T+xnyQnq4W++nhnB0q/CRJBRDWIYtaOWbqjWKZrV9i0CU6csPa4
pvgbftOrF/z4o9p4xC4ZmRn8Z8V/KBbmnYXuv/1W7dNbsqTuJO7Qv2F/Zu6YqTuGZQoVUr8A5s2z
9rim+DvIkbNHeGnZS7pjWKZ4cTXs89tv7Tvn6kOrqVC0ArVK1bLvpH42cyb07687hXu0r96efaf3
cfCM5rHGFvLHXbQp/g5SulBp3l//PonnbdjDzSb9+qn+arvM3jmbvg362ndCP0tJgUWLzCqeeREa
HEpE/QhPdf306qVGzlm5U54p/g5SKLQQPer08NSEr4gItbtXSor/zyWlZMb2GQy4cYD/T2aTJUug
aVMo550dP23xSKtHaFahme4YlilZUm3buXChdcc0xd9hvNZfWa4cNGmiipi/bfhlA4VDCxNeNtz/
J7OJGeWTP80rNqdDjQ66Y1hqwAD45hvrjmcmeTlMcmoyld+tzL7H9lG6UGndcSzx/vtqtMKXX/r3
POmZ6Rw+e5gaJWv490Q2SUtTE3w2bza7dhlqtE/t2vDLL1Dkqu2/zSQvDyhaoCida3Zmbrx3Bsj3
769GKqSm+vc8IUEhnin8AD/8oH7YTeE3AMqUgVtuUc+ArGCKvwON7TGWITcN0R3DMpUrQ8OG/t+T
1GvMKB/jalZ2/ZhuH8MW770HW7bAF1/oTuIOGRnql+bKlVCnju407ial9Mw2nomJUK8e/PrrH5f6
MN0+hmP176+WevB3149X/PCDKv6m8PvmxwM/0u9r7zwxL1cOmjdXI+h8ZYq/YYsqVaBBA/j+e+uP
nXg+kaPJR60/sEZffw2DB+tO4X7NKzZn2b5lnLxwUncUywwcaE3Xjyn+hm0GDlRFzWpj143l7dVv
W39gTdLT1RDPgQN1J3G/ogWK0q12N2bv1LDIlJ/07atWefV17owp/g6WlJLE3tN7dcewzIAB1nf9
SCn5Zvs3nprYtXw51KgBNWvqTuINg8MHM33bdN0xLFOhgpo7s3ixb8cxxd/BFiQs4LFFj+mOYRl/
dP3EHoslJT2FWyrfYt1BNTNdPtbqWbcnG45s4Ph572wuMWiQ73fRPhV/IUQpIcRiIUS8EOI7IUSJ
bF63XwjxsxBisxDCOzuV+1lE/Qh+PPAjpy+e1h3FMlb1V142NW4qQ24a4pnRHGlpagGvAd65kdGu
cGhhBocPJvZYrO4olhkwAObPhwsX8n8MX1v+zwJLpZT1gWXAc9m8LhPoKKVsJqVs5eM5A0axsGJ0
rdXVU/2VAwaojcgvXfL9WFJKpsVN486b7vT9YA7x/fdQty5Ur647ibeM6zOOzrU6645hmfLloVUr
9Qsgv3wt/pHAhKy/TwCy215aWHCugDQ4fDDT4qbpjmGZKlWgUSNrZileSLvAvU3vpXH5xr4fzCFM
l4+RW0OGwDQfSoNPk7yEEKeklKWz+/iKz+8FkoAMYLyU8tPrHNNM8rrChbQLVHqnEgl/T6BcEW8s
7ThuHCxbBtO98wzOEqmp6mFebKz6JWkY15OUpO4QDx6EkiXzPskrJKcXCCGWAOWv/BQggRev8fLs
qnZbKeWvQoiywBIhxA4p5crszjl69Ojf/t6xY0c6duyYU0zPKhxamDe6vMGFNB869xxmwAB4+mk4
dw6KeWfDLZ8tWgTh4abwGzmLiYkhJiaGihVh+PD8HcPXlv8OVF/+MSFEBWC5lLJhDu8ZBZyTUr6b
zddNyz8A9OmjujeGDdOdxDkGD4bbb4eRI3UnMdxi+nS1ZMp339m/vMNc4N6svw8Hoq9+gRCisBCi
aNbfiwDdgDgfz2u43F13wZQpulM4x5kzquVvJnb519rDa5ke553+xt69Ye3a/L3X1+I/BugqhIgH
OgNvAAghKgohLj+HLg+sFEJsBtYC86SUPk5PMNwuIgJWr4bj3hl67ZNZs6BTJyjtjS0cHCtTZjL6
h9F4pXehSBHo2TN/7/Wp+EspT0kpu0gp60spu0kpk7I+/6uUsnfW3/dJKZtmDfNsJKV8w5dzGt5w
+aLNz5j/+QnzeWThI9aH0mjyZNMFZoc2VdpwKf0Sm49u1h3FMnfmc6SzGX7pMl5psUD+u36+3PKl
p4Z3Hjmidjrr3Vt3Eu8TQjC00VC+iv1KdxTL3HFH/t5nir+LTNgygWeXPqs7hmW6dYOdO2H//ty/
59TFUyzZu4RB4YP8lstuU6eqxboKFtSdJDAMbTyUqXFTSc9M1x3FEgUK5O99pvi7SJuqbZgYO9FT
F+3gwTBpUu7fMz1uOt3rdKdkwZL+C2Yz0+VjrwZlGlCleBWW7VumO4pWpvi7SL0b6lGtRDWW7vXO
foj33qs2ds/MzN3rJ8ZOZHiTfA5sdqC4OLUxd4cOupMElhkDZ9CpRifdMbQyxd9l7m58N5Ni89BU
driWLVV3x8psp/z9LiklifTMdLrV7ub/YDb56iv1wC7I/CTaqnrJ6oQGh+qOoZXZw9dlTlw4Qe33
a3P4H4cpFuaN6bFvvw3bt8Pnn+tOYq/0dKhWTW1sf+ONutMYbmb28A0AZQqXoW+DvsQlemee3NCh
ahnj5GTdSey1aJFam8UUfkMH0/I3HKF3bzW7Nb/rlLhR377Qqxfcf7/uJIbbmZa/4VqXH/wGimPH
1HaNg7wzYtWVzqScYc2hNbpjaGGKv+EIffrA1q2wb5/uJPaYNEm1/IsX150ksB05d4T+X/f3zPDp
vDDF33CEsDA16uVarf/pcdP5dte3tmfyFynhs89gxAjdSYwby95I9ZLVPXV95ZYp/oZj3H+/Korp
VzTCpJS8uuJVCoZ4Z/rr2rWQkQHt2ulOYgD8pdlf+HxLgA01wxR/V9t3eh9PLX5KdwzLNGmihj5e
uS/p2sNruZR+iY41OmrLZbXLrX6P7DnveoPDBxOzP4Zjycd0R7GVKf4uVrFYRSb8PIF9p73TUf7g
g/Dxx79/PH7TeB5o8QDCI5Xy7FmYOTOwRjU5XbGwYvRt0JcJP0/I+cUeYoZ6utzjix6naIGivHr7
q7qjWCIlBapWVV0jN1ROouZ7NUl4JIGyRcrqjmaJsWNhxQq1UbvhHDtP7CQ5NZmWlVrqjpIv+Rnq
aYq/y8UlxtFtUjf2P76fAsH5XN7PYZ56Si13EH7XBBbtWcTU/lN1R7KElNCwIYwfD+3b605jeIkp
/gGq04ROjGwxkiE3DdEdxRK7dkHbtnDggCQj+DxFCxTVHckSS5fCE0/Azz+b/n7DWmaSV4B67JbH
+GZ7PrbEcqi6daFpU5g5U3im8AN88AE88ogp/IYzmJa/B2RkZiCRhASF6I5imdmz1YJvq1bpTmKN
AwegeXM4eFBtYWkYVjIt/wAVHBTsqcIPasbv4cOwYYPuJNb45BM1wscUfuc7kHSA5FTvrzJoir/h
SCEh8Pjj8M47upP4LiVFje1/6CHdSYzceGrJU0z8eaLuGH5nir/hKEkpSfz7h38DasbvkiV52+PX
iSZPVpvW1KmjO4mRGw/f/DBj148lU+ZyezmXMsXfcJRPN35K/Ml4AIoVU78A/vtfzaF8kJEBb74J
Tz+tO4mRWx2qd6BwaGHmxc/THcWvTPH3mLnxc/l6mztnEKVnpjN2/Vj+0fofv33u0Udh4kQ4fVpj
MB/MmQOlS5s9et1ECMFz7Z7j9ZWv4+XBJ6b4e0ypgqV47vvnXLlE7YztM6hRsgYtKrX47XOVK6uH
v+PGaQyWT1LC66/Ds8+a4Z1u07dBX06nnCZmf4zuKH5jir/H3Fb9NqoUr8LUre6aFZspM3n1x1d5
rt1zf/raU0+pZREuXdIQzAdLl8LFi+qXl+EuwUHBfB7xObVK1dIdxW9M8fegl9q/xGsrXyMjM0N3
lFxbdXAVRQsUpXud7n/6WqNG6s9Elw3AeOMNeOYZtVSF4T5tq7WlesnqumP4jZnk5UFSStp81oYn
2zzJwPCBuuPk2sW0ixQKLXTNr61ZA0OGQEKC2vjF6davV3sS794NoaG60xheZyZ5GYC6EF5s/yIL
di3QHSVPsiv8AG3aqNb/p5/aGMgH//kPPPmkKfyGc5mWv0dd/h56ZR18gE2boHdv1ZouXFh3muyt
Xv37XUpB72xAZjiYafkbvxFCeKrwg1ob59Zb4aOPdCfJnpSqn/+VV0zh95LYY7HEHovVHcNSpvgb
rvLyy/DWW3DunO4k1zZ/PiQlwd13605iWGnjLxt5eOHDnhr3b4q/oc0nP33C2HVj8/Se8HDo2tWZ
s34zMtSY/jfegOBg3WkMK93T5B6SUpKYnzA/5xe7hCn+ASI1I1V3hD84dfEUo2JG0aFG3qe+vvwy
vPeeWvXTSSZOhDJloGdP3UkMqwUHBfNG5zd49vtnXTmB8lpM8Q8AF9Mu0uCDBhw+65xqOTpmNAMa
DqBx+cZ5fm/t2mqj9yef9EOwfLpwAUaNgjFjzGxer+pZtydlC5dlwhZvbPRuin8AKBRaiMHhg3lx
2Yu6owCwLXEb0+Km8UqnV/J9jOeeU2Pply61MJgPRo+G226D1q11JzH8RQjB293e5q3VbzliAmVG
Zgafb/4833ciZqhngDh76SwNP2zI1P5TaV9d3+7hUkq6fdWNiHoR/P2Wv/t0rLlz4Z//hNhYvRO/
Nm2CHj1g61YoV05fDsMeyanJjthe9JOfPmHy1sn8eO+PBAUFmaGexrUVDyvOx70+ZkT0CM6nnteW
Iy0zjVaVWvG3ln/z+VgREVCvHvzf/1kQLJ/S09Wy02+9ZQp/oHBC4T9x4QT/Wv4vPuz5Yb6HdJuW
f4C5Z/Y9lCpYivd6vKc7iiX27oVWrWDtWj2bpbz9NixeDN99Z/r6DXtIKRk2exhlCpX57ec4P5O8
TPEPMKcvnubQ2UP5etDqVGPHwoQJarN3O7t/Lv/iWb8eanl38UfDYSZsmcCYVWP46YGfKByqprqb
Gb5GjkoVKuWpwg/wyCNQtap6CGyXlBQYPBheeMEU/kCWKTPZdXKXbeeTUrJozyKmD5j+W+HPL9Py
Nzzh1Clo1gw+/FCt/+NPUqp+/nPnYPp0090TyLYe20qXSV1YPWI1tUvX1pbDtPwNx0k8n0jvKb39
/pC5dGmYMkUVZX9P/ho/Htatg88/N4U/0DUq34h/tf8XUdOjSE5N1h0nT0zxN9h9ardfjpucmkyv
Kb1oWaklRQoU8cs5rtS2LTzxBPTqpe4E/GHNGnjpJZg9G4rqH/RhOMBDNz/EzZVu5r7o+1y19o8p
/gHu13O/0uazNqw5tMbS46ZlpDHwm4E0Ld+UUR1GWXrs6/nnP6FbN+jeHc6etfbYsbHQv79q8det
a+2xDfcSQvBRr484eOYgzy591vJfAJky09LjXWaKf4CrWKwiX0Z+SdT0KMs2q07PTOf+efcTLIL5
uPfHti4tLQS8+SbcfLO6AzhvUW/TunW/Lyjn72cKhvsUDCnIgrsWcPLiSS6mX7TsuNPipjF01lDL
jvcHUsp8/wEGAHFABtD8Oq/rDuwEEoBncjimNOz3/d7vZdk3y8qJWyb6fKxJP0+SXSd2lcmXki1I
lj8ZGVLee6+UHTpIeeyYb8datkzKsmWlnD/fkmiGkaPMzEw57qdxsvxb5eXWY1tzfH1W3cxb/c7r
G+QfC3V9oC6wLLvij7q72A1UB0KBLUCD6xzTl++ZpyxfvtzW821L3CZr/LeG/HD9hz4dJzMzU6Zn
pFuUKv/fh/R0KZ97TsqKFaVctCjv709Lk/K996QsU0ZKm/8psmX3NeFkXv1enL54Wg78eqBs/HFj
ueP4jly9Jz/F36duHyllvJRyF3C9+/pWwC4p5QEpZRowDYj05byBIiYmxtbz3Vj2Rtb8ZQ096vTw
6ThCCIKDrFvQPr/fh+BgeO01mDxZjQJ64oncbwKzYQPccot6sLtiBXTsmK8IlrP7mnAyt3wvklKS
uJR+KVevPXTmEM3GNaN8kfKsu38dDco08FsuO/r8KwOHrvj4cNbnDAeqULQCNUvV/NPn5e93ZoDq
1084mcD3e7+3M16+dOoEW7ZAYiJUqwYjRqjZwFc/lzt+HL76Su2/26cPPPYYLFsGDfz382cEgC+3
fEmjjxvx+orX+emXn667Imjl4pWZEDWBsT3HUjDEv/uAhuT0AiHEEqD8lZ8CJPCClHKev4IZzrL9
+Ha6TOpCvRvqceTsEQ6dPUT5IuW5v/n9dK7VWXe8HN1wgyrsR4+qTVdGjIBjx6BECShWTD0oPnhQ
/aLo0UPtE1y6tO7Uhhc83vpxmlZoypydc7hn9j0knk+kVqlafNDzA1pVbvWH1waJINtW3bVkhq8Q
YjnwpJRy0zW+1hoYLaXsnvXxs6j+qTHZHMs9A2UNwzAcQuZxhm+OLf88yO7EG4A6QojqwK/AEODO
7A6S1/8BwzAMI+986vMXQkQJIQ4BrYH5Qohvsz5fUQgxH0BKmQE8AiwGtgHTpJQ7fIttGIZh+MJx
C7sZhmEY/ueYGb5CiO5CiJ1CiAQhxDO68+gihKgihFgmhNgmhNgqhHhUdybdhBBBQohNQoi5urPo
JIQoIYT4RgixI+v6uEV3Jl2EEP8QQsQJIWKFEJOFEAV0Z7KLEOIzIcQxIUTsFZ8rJYRYLISIF0J8
J4QokdNxHFH8hRBBwAfAHUA4cKcQIlAH2KUDT0gpw4E2wMMB/L247DFgu+4QDvAesFBK2RBoAgRk
96kQohLwd9TE0saoZ5dD9Kay1ReoWnmlZ4GlUsr6qEm3Oe5u4Yjij5kI9hsp5VEp5ZasvyejfsAD
dl6EEKIK0BP4n+4sOgkhigO3SSm/AJBSpkspLV66zlWCgSJCiBCgMPCL5jy2kVKuBE5f9elIYELW
3ycAUTkdxynF30wEuwYhRA2gKbBObxKt/g/4J2puSSCrCZwQQnyR1QU2XghRSHcoHaSUvwDvAAeB
I0CSlHKp3lTalZNSHgPVgATK5fQGpxR/4ypCiKLADOCxrDuAgCOE6AUcy7oTElx/GRGvCwGaAx9K
KZsDF1C3+gFHCFES1dKtDlQCigoh7tKbynFybCw5pfgfAapd8XGVrM8FpKxb2RnAJClltO48GrUF
IoQQe4GpQCchxETNmXQ5DBySUv6U9fEM1C+DQNQF2CulPJU1lHwWcKvmTLodE0KUBxBCVAASc3qD
U4r/bxPBsp7aDwECeWTH58B2KeV7uoPoJKV8XkpZTUpZC3VNLJNS3qM7lw5Zt/SHhBD1sj7VmcB9
CH4QaC2EKCjUZhGdCbyH31ffCc8F7s36+3Agx0ajlTN8801KmSGEuDwRLAj4LFAnggkh2gJDga1C
iM2o27fnpZSL9CYzHOBRYLIQIhTYC9ynOY8WUsr1QogZwGYgLeu/4/Wmso8QYgrQEbhBCHEQGAW8
AXwjhBgBHAAG5XgcM8nLMAwj8Dil28cwDMOwkSn+hmEYAcgUf8MwjABkir9hGEYAMsXfMAwjAJni
bxiGEYBM8TcMwwhApvgbhmEEoP8Hf41iEpQega0AAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>