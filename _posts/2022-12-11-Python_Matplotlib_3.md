---
layout: post
title: "Python - matplotlib_3"
categories: python
author: "aureusoh"
meta: "Springfield"
---
<style type="text/css">
     pre { line-height: 125%;}
     td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
     span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
     td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
     span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
     .highlight .hll { background-color: var(--jp-cell-editor-active-background) }
     .highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color); }
     .highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
     .highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
     .highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
     .highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
     .highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
     .highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
     .highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
     .highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
     .highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
     .highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
     .highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
     .highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
     .highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
     .highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
     .highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
     .highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
     .highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
     .highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
     .highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
     .highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
     .highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
     .highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
     .highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
     .highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
     .highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
     .highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
     .highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
     .highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
     .highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
     .highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
     .highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
     .highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
     .highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
     .highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
     .highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
     .highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
     .highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
     .highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
     .highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
     .highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
</style>
<style type="text/css">
     :root {
          --jp-layout-color0: white;
          --jp-layout-color1: white;

          --jp-content-font-color0: rgba(0, 0, 0, 1);
          --jp-content-font-color1: rgba(0, 0, 0, 0.87);
          --jp-content-font-color2: rgba(0, 0, 0, 0.54);
          --jp-content-font-color3: rgba(0, 0, 0, 0.38);

          --jp-mirror-editor-keyword-color: #008000;
          --jp-mirror-editor-atom-color: #88f;
          --jp-mirror-editor-number-color: #080;
          --jp-mirror-editor-def-color: #00f;
          --jp-mirror-editor-variable-color: var(--md-grey-900);
          --jp-mirror-editor-variable-2-color: #05a;
          --jp-mirror-editor-variable-3-color: #085;
          --jp-mirror-editor-punctuation-color: #05a;
          --jp-mirror-editor-property-color: #05a;
          --jp-mirror-editor-operator-color: #aa22ff;
          --jp-mirror-editor-comment-color: #408080;
          --jp-mirror-editor-string-color: #ba2121;
          --jp-mirror-editor-string-2-color: #708;
          --jp-mirror-editor-meta-color: #aa22ff;
          --jp-mirror-editor-qualifier-color: #555;
          --jp-mirror-editor-builtin-color: #008000;
          --jp-mirror-editor-bracket-color: #997;
          --jp-mirror-editor-tag-color: #170;
          --jp-mirror-editor-attribute-color: #00c;
          --jp-mirror-editor-header-color: blue;
          --jp-mirror-editor-quote-color: #090;
          --jp-mirror-editor-link-color: #00c;
          --jp-mirror-editor-error-color: #f00;
          --jp-mirror-editor-hr-color: #999;

          /* Cell specific styles */

          --jp-cell-padding: 5px;

          --jp-cell-collapser-width: 8px;
          --jp-cell-collapser-min-height: 20px;
          --jp-cell-collapser-not-active-hover-opacity: 0.6;

          --jp-cell-editor-background: var(--md-grey-200);
          --jp-cell-editor-border-color: var(--md-grey-300);
          --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
          --jp-cell-editor-active-background: var(--jp-layout-color0);
          --jp-cell-editor-active-border-color: var(--jp-brand-color1);

          --jp-cell-prompt-width: 64px;
          --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
          --jp-cell-prompt-letter-spacing: 0px;
          --jp-cell-prompt-opacity: 1;
          --jp-cell-prompt-not-active-opacity: 0.5;
          --jp-cell-prompt-not-active-font-color: var(--md-grey-700);

          /* A custom blend of MD grey and blue 600
          * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
          --jp-cell-inprompt-font-color: #307fc1;
          /* A custom blend of MD grey and orange 600
          * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
          --jp-cell-outprompt-font-color: #bf5b3d;

          /*
          * Code Fonts
          *
          * Code font variables are used for typography of code and other monospaces content.
          */

          --jp-code-font-size: 13px;
          --jp-code-line-height: 1.3077; /* 17px for 13px base */
          --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
          --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
          --jp-code-font-family: var(--jp-code-font-family-default);

          --md-grey-50: #fafafa;
          --md-grey-100: #f5f5f5;
          --md-grey-200: #eeeeee;
          --md-grey-300: #e0e0e0;
          --md-grey-400: #bdbdbd;
          --md-grey-500: #9e9e9e;
          --md-grey-600: #757575;
          --md-grey-700: #616161;
          --md-grey-800: #424242;
          --md-grey-900: #212121;
     }
</style>
<style type="text/css">

     pre {
          margin: 0px;
          padding: 0px;
          background-color: transparent;
     }

     .jp-InputArea, .jp-OutputArea-child {
          display: flex;
          flex-direction: row;
          padding: 0px;
          margin: 0px;
          overflow: visible;
     }

     @media (max-width: 767px) {
          .jp-InputArea, .jp-OutputArea-child {
               flex-direction: column;
          }
     }

     .jp-InputPrompt, .jp-OutputPrompt {
          flex: 0 0 64px;
          color: var(--jp-cell-inprompt-font-color);
          font-family: var(--jp-cell-prompt-font-family);
          padding: var(--jp-code-padding);
          font-size: var(--jp-code-font-size);
          border: var(--jp-border-width) solid transparent;
          text-align: right;
          white-space: nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
          -webkit-user-select: none;
          -moz-user-select: none;
          -ms-user-select: none;
          user-select: none;
     }

     @media (max-width: 767px) {
          .jp-InputPrompt {
               flex: auto;
               text-align: left;
          }
     }
     .CodeMirror {
          flex-grow: 1;
          margin: 0px;
          padding: var(--jp-code-padding);
          border: 1px solid var(--jp-cell-editor-border-color);
          background: var(--jp-cell-editor-background);
     }

     .jp-RenderedText, .jp-RenderedImage {
          flex-grow: 1;
          margin: 0px;
          padding: var(--jp-code-padding);
     }

</style>


# Python matplotlib

## 1. 개요

MATLAB은 simulink도 압도적인 역할을 하지만, graph 기능 또한 탁월합니다. 마치 Photoshop을 그림 배경 지우는 용도로만 사용하시는 분들이 있듯이, MATLAB을 graph 그리는 분들도 더러있습니다. 그러나, 단순히 graph를 그리는 용도로만 MATLAB을 쓰기에는 너무나도 비쌉니다.
matplotlib를 이용하면 MATLAB과 유사하게 graph를 그릴 수 있습니다. Excel의 graph로는 부족하신분들, 데이터 분석하시는분들에게 필수적인 라이브러리입니다.

! matplotlib에서 사용하는 기본 자료형은 numpy를 이용합니다. 아직 numpy가 익숙하지 않으신 분들은 numpy를 보신 후 다시 보시기를 권장합니다.

## 2. Graph

1.
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

<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">cos</span><span class="p">(</span><span class="n">x</span><span class="p">))</span>
</pre></div>
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