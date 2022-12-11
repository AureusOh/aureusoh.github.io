---
layout: post
title: "Python - matplotlib"
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
     }

     .jp-Cell-inputWrapper, .jp-Cell-outputWrapper {
          display: flex;
          flex-direction: row;
          padding: 0px;
          margin: 0px;
          /* Added to reveal the box-shadow on the input and output collapsers. */
          overflow: visible;
     }

     @media (max-width: 767px) {
          .jp-Cell-inputWrapper {
               flex-direction: column;
          }
     }

     .jp-InputPrompt {
          flex: 0 0 64px;
          color: var(--jp-cell-inprompt-font-color);
          font-family: var(--jp-cell-prompt-font-family);
          padding: var(--jp-code-padding);
          letter-spacing: var(--jp-cell-prompt-letter-spacing);
          opacity: var(--jp-cell-prompt-opacity);
          line-height: var(--jp-code-line-height);
          font-size: var(--jp-code-font-size);
          border: var(--jp-border-width) solid transparent;
          opacity: var(--jp-cell-prompt-opacity);
          /* Right align prompt text, don't wrap to handle large prompt numbers */
          text-align: right;
          white-space: nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
          /* Disable text selection */
          -webkit-user-select: none;
          -moz-user-select: none;
          -ms-user-select: none;
          user-select: none;
     }

     div.CodeMirror {
          flex-grow: 1;
          margin: 0px;
          padding: 5px;
          border: 1px solid var(--jp-cell-editor-border-color);
          background: var(--jp-cell-editor-background);
     }

</style>

## 1. 개요

MATLAB은 simulink도 압도적인 역할을 하지만, graph 기능 또한 탁월합니다. 마치 Photoshop을 그림 배경 지우는 용도로만 사용하시는 분들이 있듯이, MATLAB을 graph 그리는 분들도 더러있습니다. 그러나, 단순히 graph를 그리는 용도로만 MATLAB을 쓰기에는 너무나도 비쌉니다.

matplotlib를 이용하면 MATLAB과 유사하게 graph를 그릴 수 있습니다. Excel의 graph로는 부족하신분들, 데이터 분석하시는분들에게 필수적인 라이브러리입니다.

! matplotlib에서 사용하는 기본 자료형은 numpy를 이용합니다. 아직 numpy가 익숙하지 않으신 분들은 numpy를 보신 후 다시 보시기를 권장합니다.

## 2. 그래프 그리기

<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
</pre></div>
</div>
</div>
</div>
</div>

`matplotlib.pyplot`과 `numpy`를 임포트해줍니다. 일반적으로 `plt`과 `np`이름을 사용합니다.

<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> <span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">linspace</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">100</span><span class="p">)</span>
 <span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">sin</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>

sine 함수를 그려보도록 하겠습니다. x값과 y값을 만들어줍니다.


## 3. 그래프 서식