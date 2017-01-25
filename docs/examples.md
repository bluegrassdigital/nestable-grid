## Using breakpoints and output-sizes

Custom gutter width and custom breakpoints and output sizes

<?codeblock external="example.scss" title="SCSS" lang="scss"></codeblock?>

<?tabs>
<codeembed title="Result" size="desktop" base="grid.html" stylesheets="helpers.css,example.css" adjust-height use-html="grid"></codeembed>
<codeblock title="HTML" lang="html" ref="grid">
  <div class="cs">
    <div class="cols-l-6 cols-xl-3"></div>
    <div class="cols-l-6 cols-xl-9"></div>
    <div class="cols-l-6 cols-xl-9">
      <div class="cs">
        <div class="cols-xl-3"></div>
        <div class="cols-l-6">
          <div class="cs">
            <div class="cols-xl-3"></div>
            <div class="cols-xl-3"></div>
          </div>
        </div>
        <div class="cols-xl-3"></div>
        <div class="cols-xl-3"></div>
        <div class="cols-xl-3"></div>
      </div>
    </div>
    <div class="cols-l-6 cols-xl-3"></div>
  </div>
</codeblock>
<codeblock external="example.css" title="Generated CSS" lang="css"></codeblock>
</tabs?>

## Emulating bootstrap classes and sizes (static gutter width)

<?codeblock external="example-bootstrap.scss" title="SCSS" lang="scss"></codeblock?>

<?tabs>
<codeembed title="Result" size="desktop" base="iframe.html" stylesheets="helpers.css,example-bootstrap.css" adjust-height use-html="grid-2"></codeembed>
<codeblock title="HTML" lang="html" ref="grid-2">
  <div class="row">
    <div class="col-md-6 col-lg-3"></div>
    <div class="col-md-6 col-lg-9"></div>
    <div class="col-md-6 col-lg-9">
      <div class="row">
        <div class="col-lg-3"></div>
        <div class="col-md-6">
          <div class="row">
            <div class="col-lg-3"></div>
            <div class="col-lg-3"></div>
          </div>
        </div>
        <div class="col-lg-3"></div>
        <div class="col-lg-3"></div>
        <div class="col-lg-3"></div>
      </div>
    </div>
    <div class="col-md-6 col-lg-3"></div>
  </div>
</codeblock>
<codeblock external="example-bootstrap.css" title="Generated CSS" lang="css"></codeblock>
</tabs?>

## Nest as many levels deep as you like

The only restriction is on the total column count. Bear in mind that side effects will occur if you try and nest a larger column set inside a smaller one at a particular breakpoint - i.e. you can't put a `.cols-l-8` inside a `.cols-xl-6`, assuming both of those are the sizes that are currently applied it will get confused.

<?codeblock title="HTML" lang="html" ref="grid-3">
  <div class="cs">
    <div class="cols-l-6 cols-xl-12"></div>
    <div class="cols-l-6 cols-xl-12">
      <div class="cs">
        <div class="cols-l-4 cols-xl-10">
          <div class="cs">
            <div class="cols-xl-8">
              <div class="cs">
                <div class="cols-xl-6">
                  <div class="cs">
                    <div class="cols-xl-4">
                      <div class="cs">
                        <div class="cols-xl-2"></div>
                        <div class="cols-l-2"></div>
                      </div>
                    </div>
                    <div class="cols-l-2"></div>
                  </div>
                </div>
                <div class="cols-l-2"></div>
              </div>
            </div>
            <div class="cols-l-2"></div>
          </div>
        </div>
        <div class="cols-l-2"></div>
      </div>
    </div>
  </div>
</codeblock?>

<?codeembed title="Result" size="desktop" base="iframe.html" stylesheets="helpers.css,example-nested.css" adjust-height use-html="grid-3"></codeembed?>

## Different number of columns

<?codeblock external="example-columns.scss" title="SCSS" lang="scss"></codeblock?>

<?tabs>
<codeembed title="Result" size="desktop" base="iframe.html" stylesheets="helpers.css,example-columns.css" adjust-height use-html="grid-4"></codeembed>
<codeblock title="HTML" lang="html" ref="grid-4">
  <div class="cs">
    <div class="cols-l-6 cols-xl-3"></div>
    <div class="cols-l-12 cols-xl-15"></div>
    <div class="cols-l-6 cols-xl-15">
      <div class="cs">
        <div class="cols-xl-3"></div>
        <div class="cols-l-12">
          <div class="cs">
            <div class="cols-xl-6"></div>
            <div class="cols-xl-6"></div>
          </div>
        </div>
        <div class="cols-xl-6"></div>
        <div class="cols-xl-3"></div>
        <div class="cols-xl-6"></div>
      </div>
    </div>
    <div class="cols-l-12 cols-xl-3"></div>
  </div>
</codeblock>
<codeblock external="example-columns.css" title="Generated CSS" lang="css"></codeblock>
</tabs?>
