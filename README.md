# api documentation for  [pdf2json (v1.1.7)](https://github.com/modesty/pdf2json)  [![npm package](https://img.shields.io/npm/v/npmdoc-pdf2json.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pdf2json) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pdf2json.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pdf2json)
#### A PDF file parser that converts PDF binaries to text based JSON, powered by porting a fork of PDF.JS to Node.js

[![NPM](https://nodei.co/npm/pdf2json.png?downloads=true)](https://www.npmjs.com/package/pdf2json)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pdf2json/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pdf2json_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pdf2json/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pdf2json/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pdf2json/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Modesty Zhang",
        "email": "modestyz@hotmail.com",
        "url": "http://www.codeproject.com/script/Articles/MemberArticles.aspx?amid=62372"
    },
    "bin": {
        "pdf2json": "./bin/pdf2json"
    },
    "bugs": {
        "url": "http://github.com/modesty/pdf2json/issues"
    },
    "bundleDependencies": [
        "xmldom",
        "lodash",
        "optimist",
        "async"
    ],
    "contributors": [],
    "dependencies": {
        "async": "^2.0.1",
        "lodash": "^4.15.0",
        "optimist": "^0.6.1",
        "xmldom": "^0.1.22"
    },
    "description": "A PDF file parser that converts PDF binaries to text based JSON, powered by porting a fork of PDF.JS to Node.js",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "a09d705ce64d82cbc7d0473d1424963f751bec32",
        "tarball": "https://registry.npmjs.org/pdf2json/-/pdf2json-1.1.7.tgz"
    },
    "engines": {
        "node": ">=4.0"
    },
    "gitHead": "c5551c298e49564a8c4d8fb0af8ed97f2f4ecfdc",
    "homepage": "https://github.com/modesty/pdf2json",
    "keywords": [
        "pdf",
        "pdf parser",
        "convert pdf to json",
        "server side PDF parser",
        "port pdf.js to node.js",
        "PDF binary to text",
        "commandline utility to parse pdf to json",
        "JSON",
        "javascript",
        "PDF canvas",
        "pdf.js fork"
    ],
    "licenses": [
        {
            "type": "Apache v2",
            "url": "https://github.com/modesty/pdf2json/blob/master/license.txt"
        }
    ],
    "main": "./pdfparser.js",
    "maintainers": [
        {
            "name": "modesty",
            "email": "modestyz@gmail.com"
        }
    ],
    "name": "pdf2json",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/modesty/pdf2json.git"
    },
    "scripts": {
        "test": "cd ./test && sh p2j.forms.sh",
        "test-misc": "node pdf2json.js -f ./test/pdf/misc/ -o ./test/target/misc/ -c -m"
    },
    "version": "1.1.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pdf2json](#apidoc.module.pdf2json)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>p2jcmd ()](#apidoc.element.pdf2json.p2jcmd)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdf (needRawText)](#apidoc.element.pdf2json.pdf)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfanno (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdfanno)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfcanvas (canvasTarget, scaledWidth, scaledHeight)](#apidoc.element.pdf2json.pdfcanvas)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffield (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdffield)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffill (x, y, width, height, color)](#apidoc.element.pdf2json.pdffill)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffont (fontObj)](#apidoc.element.pdf2json.pdffont)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfline (x1, y1, x2, y2, lineWidth, color, dashed)](#apidoc.element.pdf2json.pdfline)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfunit ()](#apidoc.element.pdf2json.pdfunit)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>ptixmlinject ()](#apidoc.element.pdf2json.ptixmlinject)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>super_ (options)](#apidoc.element.pdf2json.super_)
1.  object <span class="apidocSignatureSpan">pdf2json.</span>p2jcmd.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdf.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdfanno.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdfcanvas.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdffield.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdffill.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdffont.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>pdfline.prototype
1.  object <span class="apidocSignatureSpan">pdf2json.</span>ptixmlinject.prototype

#### [module pdf2json.p2jcmd](#apidoc.module.pdf2json.p2jcmd)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>p2jcmd ()](#apidoc.element.pdf2json.p2jcmd.p2jcmd)

#### [module pdf2json.p2jcmd.prototype](#apidoc.module.pdf2json.p2jcmd.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>complete (err)](#apidoc.element.pdf2json.p2jcmd.prototype.complete)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>initialize ()](#apidoc.element.pdf2json.p2jcmd.prototype.initialize)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processFiles (inputDir, files)](#apidoc.element.pdf2json.p2jcmd.prototype.processFiles)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processOneDirectory ()](#apidoc.element.pdf2json.p2jcmd.prototype.processOneDirectory)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processOneFile ()](#apidoc.element.pdf2json.p2jcmd.prototype.processOneFile)
1.  [function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>start ()](#apidoc.element.pdf2json.p2jcmd.prototype.start)

#### [module pdf2json.pdf](#apidoc.module.pdf2json.pdf)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdf (needRawText)](#apidoc.element.pdf2json.pdf.pdf)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.</span>super_ ()](#apidoc.element.pdf2json.pdf.super_)

#### [module pdf2json.pdf.prototype](#apidoc.module.pdf2json.pdf.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>destroy ()](#apidoc.element.pdf2json.pdf.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getAllFieldsTypes ()](#apidoc.element.pdf2json.pdf.prototype.getAllFieldsTypes)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getMergedTextBlocksIfNeeded ()](#apidoc.element.pdf2json.pdf.prototype.getMergedTextBlocksIfNeeded)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getRawTextContent ()](#apidoc.element.pdf2json.pdf.prototype.getRawTextContent)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>load (pdfDocument, scale)](#apidoc.element.pdf2json.pdf.prototype.load)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>loadMetaData ()](#apidoc.element.pdf2json.pdf.prototype.loadMetaData)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>loadPages ()](#apidoc.element.pdf2json.pdf.prototype.loadPages)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parseMetaData ()](#apidoc.element.pdf2json.pdf.prototype.parseMetaData)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parsePDFData (arrayBuffer)](#apidoc.element.pdf2json.pdf.prototype.parsePDFData)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parsePage (promisedPages, id, scale)](#apidoc.element.pdf2json.pdf.prototype.parsePage)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>raiseErrorEvent (errMsg)](#apidoc.element.pdf2json.pdf.prototype.raiseErrorEvent)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>raiseReadyEvent (data)](#apidoc.element.pdf2json.pdf.prototype.raiseReadyEvent)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>tryLoadFieldInfoXML (pdfFilePath)](#apidoc.element.pdf2json.pdf.prototype.tryLoadFieldInfoXML)

#### [module pdf2json.pdfanno](#apidoc.module.pdf2json.pdfanno)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfanno (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdfanno.pdfanno)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfanno.</span>processAnnotation (annotation, item)](#apidoc.element.pdf2json.pdfanno.processAnnotation)

#### [module pdf2json.pdfanno.prototype](#apidoc.module.pdf2json.pdfanno.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfanno.prototype.</span>clean ()](#apidoc.element.pdf2json.pdfanno.prototype.clean)

#### [module pdf2json.pdfcanvas](#apidoc.module.pdf2json.pdfcanvas)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfcanvas (canvasTarget, scaledWidth, scaledHeight)](#apidoc.element.pdf2json.pdfcanvas.pdfcanvas)

#### [module pdf2json.pdfcanvas.prototype](#apidoc.module.pdf2json.pdfcanvas.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>arc (aX, aY, aRadius, aStartAngle, aEndAngle, aClockwise)](#apidoc.element.pdf2json.pdfcanvas.prototype.arc)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>arcTo ()](#apidoc.element.pdf2json.pdfcanvas.prototype.arcTo)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>beginPath ()](#apidoc.element.pdf2json.pdfcanvas.prototype.beginPath)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>bezierCurveTo (aCP1x, aCP1y, aCP2x, aCP2y, aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.bezierCurveTo)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>clearRect ()](#apidoc.element.pdf2json.pdfcanvas.prototype.clearRect)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>clip ()](#apidoc.element.pdf2json.pdfcanvas.prototype.clip)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>closePath ()](#apidoc.element.pdf2json.pdfcanvas.prototype.closePath)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createLinearGradient (aX0, aY0, aX1, aY1)](#apidoc.element.pdf2json.pdfcanvas.prototype.createLinearGradient)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createPattern ()](#apidoc.element.pdf2json.pdfcanvas.prototype.createPattern)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createRadialGradient (aX0, aY0, aR0, aX1, aY1, aR1)](#apidoc.element.pdf2json.pdfcanvas.prototype.createRadialGradient)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>drawImage (image, var_args)](#apidoc.element.pdf2json.pdfcanvas.prototype.drawImage)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fill ()](#apidoc.element.pdf2json.pdfcanvas.prototype.fill)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fillRect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.fillRect)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fillText (text, x, y, maxWidth, fontSize)](#apidoc.element.pdf2json.pdfcanvas.prototype.fillText)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getContext (ctxType)](#apidoc.element.pdf2json.pdfcanvas.prototype.getContext)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getCoords_ (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.getCoords_)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getImageData (x, y, w, h)](#apidoc.element.pdf2json.pdfcanvas.prototype.getImageData)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getLineDash ()](#apidoc.element.pdf2json.pdfcanvas.prototype.getLineDash)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>lineTo (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.lineTo)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>measureText (text)](#apidoc.element.pdf2json.pdfcanvas.prototype.measureText)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>moveTo (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.moveTo)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>quadraticCurveTo (aCPx, aCPy, aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.quadraticCurveTo)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>rect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.rect)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>restore ()](#apidoc.element.pdf2json.pdfcanvas.prototype.restore)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>rotate (aRot)](#apidoc.element.pdf2json.pdfcanvas.prototype.rotate)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>save ()](#apidoc.element.pdf2json.pdfcanvas.prototype.save)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>scale (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.scale)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setFont (fontObj)](#apidoc.element.pdf2json.pdfcanvas.prototype.setFont)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setLineDash (lineDash)](#apidoc.element.pdf2json.pdfcanvas.prototype.setLineDash)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setTransform (m11, m12, m21, m22, dx, dy)](#apidoc.element.pdf2json.pdfcanvas.prototype.setTransform)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>stroke (aFill)](#apidoc.element.pdf2json.pdfcanvas.prototype.stroke)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>strokeRect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.strokeRect)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>strokeText (text, x, y, maxWidth)](#apidoc.element.pdf2json.pdfcanvas.prototype.strokeText)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>transform (m11, m12, m21, m22, dx, dy)](#apidoc.element.pdf2json.pdfcanvas.prototype.transform)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>translate (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.translate)

#### [module pdf2json.pdffield](#apidoc.module.pdf2json.pdffield)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffield (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdffield.pdffield)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>getAllFieldsTypes (data)](#apidoc.element.pdf2json.pdffield.getAllFieldsTypes)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>isFormElement (field)](#apidoc.element.pdf2json.pdffield.isFormElement)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>isWidgetSupported (field)](#apidoc.element.pdf2json.pdffield.isWidgetSupported)

#### [module pdf2json.pdffield.prototype](#apidoc.module.pdf2json.pdffield.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffield.prototype.</span>clean ()](#apidoc.element.pdf2json.pdffield.prototype.clean)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffield.prototype.</span>processField ()](#apidoc.element.pdf2json.pdffield.prototype.processField)

#### [module pdf2json.pdffill](#apidoc.module.pdf2json.pdffill)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffill (x, y, width, height, color)](#apidoc.element.pdf2json.pdffill.pdffill)

#### [module pdf2json.pdffill.prototype](#apidoc.module.pdf2json.pdffill.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffill.prototype.</span>processFill (targetData)](#apidoc.element.pdf2json.pdffill.prototype.processFill)

#### [module pdf2json.pdffont](#apidoc.module.pdf2json.pdffont)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdffont (fontObj)](#apidoc.element.pdf2json.pdffont.pdffont)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>areAdjacentBlocks (t1, t2)](#apidoc.element.pdf2json.pdffont.areAdjacentBlocks)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>areDuplicateBlocks (t1, t2)](#apidoc.element.pdf2json.pdffont.areDuplicateBlocks)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>compareBlockPos (t1, t2)](#apidoc.element.pdf2json.pdffont.compareBlockPos)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>getFontSize (textBlock)](#apidoc.element.pdf2json.pdffont.getFontSize)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>getSpaceThreshHold (t1)](#apidoc.element.pdf2json.pdffont.getSpaceThreshHold)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>haveSameStyle (t1, t2)](#apidoc.element.pdf2json.pdffont.haveSameStyle)

#### [module pdf2json.pdffont.prototype](#apidoc.module.pdf2json.pdffont.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>clean ()](#apidoc.element.pdf2json.pdffont.prototype.clean)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>flash_encode (str)](#apidoc.element.pdf2json.pdffont.prototype.flash_encode)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>processText (p, str, maxWidth, color, fontSize, targetData, matrix2D)](#apidoc.element.pdf2json.pdffont.prototype.processText)

#### [module pdf2json.pdfline](#apidoc.module.pdf2json.pdfline)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfline (x1, y1, x2, y2, lineWidth, color, dashed)](#apidoc.element.pdf2json.pdfline.pdfline)

#### [module pdf2json.pdfline.prototype](#apidoc.module.pdf2json.pdfline.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfline.prototype.</span>processLine (targetData)](#apidoc.element.pdf2json.pdfline.prototype.processLine)

#### [module pdf2json.pdfunit](#apidoc.module.pdf2json.pdfunit)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>pdfunit ()](#apidoc.element.pdf2json.pdfunit.pdfunit)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>colorCount ()](#apidoc.element.pdf2json.pdfunit.colorCount)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>findColorIndex (color)](#apidoc.element.pdf2json.pdfunit.findColorIndex)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>getColorByIndex (clrId)](#apidoc.element.pdf2json.pdfunit.getColorByIndex)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>pointToPixel (point)](#apidoc.element.pdf2json.pdfunit.pointToPixel)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFixedFloat (fNum)](#apidoc.element.pdf2json.pdfunit.toFixedFloat)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormPoint (viewportX, viewportY)](#apidoc.element.pdf2json.pdfunit.toFormPoint)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormX (viewportX)](#apidoc.element.pdf2json.pdfunit.toFormX)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormY (viewportY)](#apidoc.element.pdf2json.pdfunit.toFormY)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toPixelX (formX)](#apidoc.element.pdf2json.pdfunit.toPixelX)
1.  [function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toPixelY (formY)](#apidoc.element.pdf2json.pdfunit.toPixelY)

#### [module pdf2json.ptixmlinject](#apidoc.module.pdf2json.ptixmlinject)
1.  [function <span class="apidocSignatureSpan">pdf2json.</span>ptixmlinject ()](#apidoc.element.pdf2json.ptixmlinject.ptixmlinject)

#### [module pdf2json.ptixmlinject.prototype](#apidoc.module.pdf2json.ptixmlinject.prototype)
1.  [function <span class="apidocSignatureSpan">pdf2json.ptixmlinject.prototype.</span>getFields (pageNum)](#apidoc.element.pdf2json.ptixmlinject.prototype.getFields)
1.  [function <span class="apidocSignatureSpan">pdf2json.ptixmlinject.prototype.</span>parseXml (filePath, callback)](#apidoc.element.pdf2json.ptixmlinject.prototype.parseXml)



# <a name="apidoc.module.pdf2json"></a>[module pdf2json](#apidoc.module.pdf2json)

#### <a name="apidoc.element.pdf2json.p2jcmd"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>p2jcmd ()](#apidoc.element.pdf2json.p2jcmd)
- description and source-code
```javascript
p2jcmd = function () {
    this.inputCount = 0;
    this.successCount = 0;
    this.failedCount = 0;
    this.warningCount = 0;

    this.p2j = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdf"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdf (needRawText)](#apidoc.element.pdf2json.pdf)
- description and source-code
```javascript
pdf = function (needRawText) {
    nodeEvents.EventEmitter.call(this);
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = () => _id;
    this.get_name = () => _name + _id;

    // public, this instance copies
    this.pdfDocument = null;
    this.pages = [];
    this.pageWidth = 0;
    this.rawTextContents = [];

    this.needRawText = needRawText;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfanno"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfanno (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdfanno)
- description and source-code
```javascript
pdfanno = function (field, viewport, Fields, Boxsets) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function () {
        return _id;
    };
    this.get_name = function () {
        return _name + _id;
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfcanvas (canvasTarget, scaledWidth, scaledHeight)](#apidoc.element.pdf2json.pdfcanvas)
- description and source-code
```javascript
function CanvasRenderingContext2D_(canvasTarget, scaledWidth, scaledHeight) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.m_ = createMatrixIdentity();

    this.mStack_ = [];
    this.aStack_ = [];
    this.currentPath_ = [];

    // Canvas context properties
    this.strokeStyle = '#000';
    this.fillStyle = '#000';

    this.lineWidth = 1;
    this.lineJoin = 'miter';
    this.lineCap = 'butt';
    this.dashArray = [];
    this.miterLimit = 1;
    this.globalAlpha = 1;

    if (!_.has(canvasTarget, "HLines") || !_.isArray(canvasTarget.HLines))
        canvasTarget.HLines = [];
    if (!_.has(canvasTarget, "VLines") || !_.isArray(canvasTarget.VLines))
        canvasTarget.VLines = [];
    if (!_.has(canvasTarget, "Fills") || !_.isArray(canvasTarget.Fills))
        canvasTarget.Fills = [];
    if (!_.has(canvasTarget, "Texts") || !_.isArray(canvasTarget.Texts))
        canvasTarget.Texts = [];

    this.canvas = canvasTarget;

    this.width = scaledWidth;
    this.height = scaledHeight;

    this.arcScaleX_ = 1;
    this.arcScaleY_ = 1;
    this.lineScale_ = 1;

    this.currentFont = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffield"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffield (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdffield)
- description and source-code
```javascript
pdffield = function (field, viewport, Fields, Boxsets) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.field = field;
    this.viewport = viewport;
    this.Fields = Fields;
    this.Boxsets = Boxsets;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffill"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffill (x, y, width, height, color)](#apidoc.element.pdf2json.pdffill)
- description and source-code
```javascript
pdffill = function (x, y, width, height, color) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.x = x;
    this.y = y;
    this.width = width;
    this.height = height;
    this.color = color;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffont"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffont (fontObj)](#apidoc.element.pdf2json.pdffont)
- description and source-code
```javascript
pdffont = function (fontObj) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.fontObj = fontObj;
    let typeName = (fontObj.name || fontObj.fallbackName);
    if (!typeName) {
        typeName = _kFontFaces[0]; //default font family name
    }
    typeName = typeName.toLowerCase();
    this.typeName = typeName;

    let subType = typeName;
    let nameArray = typeName.split('+');
    if (_.isArray(nameArray) && nameArray.length > 1) {
        subType = nameArray[1].split("-");
        if (_.isArray(subType) && subType.length > 1) {
            if (!this.bold) {
                let subName = subType[1].toLowerCase();
                this.bold = _boldSubNames.indexOf(subName) >= 0;
            }
            subType = subType[0];
        }
    }
    this.subType = subType;

    this.isSymbol = typeName.indexOf("symbol") > 0 || _kFontFaces[2].indexOf(this.subType) >= 0;
    if (this.fontObj.isSymbolicFont) {
        let mFonts = _stdFonts.filter( (oneName) => (typeName.indexOf(oneName) >= 0) );

        if (mFonts.length > 0) {
            this.fontObj.isSymbolicFont = false; //lots of Arial-based font is detected as symbol in VA forms (301, 76-c, etc.)
reset the flag for now
            nodeUtil.p2jinfo("Reset: isSymbolicFont (false) for " + this.fontObj.name);
        }
    }
    else {
        if (this.isSymbol) {
            this.fontObj.isSymbolicFont = true; //text pdf: va_ind_760c
            nodeUtil.p2jinfo("Reset: isSymbolicFont (true) for " + this.fontObj.name);
        }
    }

    this.fontSize = 1;

    this.faceIdx = 0;
    this.bold = false;
    this.italic = false;

    this.fontStyleId = -1;

	    this.spaceWidth = fontObj.spaceWidth;
	    if (!this.spaceWidth) {
		    var spaceId = Array.isArray(fontObj.toFontChar) ? fontObj.toFontChar.indexOf(32) : -1;
		    this.spaceWidth = (spaceId >= 0 && Array.isArray(fontObj.widths)) ? fontObj.widths[spaceId] : 250;
	    }
	    this.spaceWidth = PDFUnit.toFormX(this.spaceWidth) / 32;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfline"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfline (x1, y1, x2, y2, lineWidth, color, dashed)](#apidoc.element.pdf2json.pdfline)
- description and source-code
```javascript
pdfline = function (x1, y1, x2, y2, lineWidth, color, dashed) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.x1 = x1;
    this.y1 = y1;
    this.x2 = x2;
    this.y2 = y2;
    this.lineWidth = lineWidth || 1.0;
    this.color = color;
    this.dashed = dashed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfunit ()](#apidoc.element.pdf2json.pdfunit)
- description and source-code
```javascript
pdfunit = function () {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.ptixmlinject"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>ptixmlinject ()](#apidoc.element.pdf2json.ptixmlinject)
- description and source-code
```javascript
ptixmlinject = function () {
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.super_"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>super_ (options)](#apidoc.element.pdf2json.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform))
    return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function')
      this._transform = options.transform;

    if (typeof options.flush === 'function')
      this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function() {
    if (typeof this._flush === 'function')
      this._flush(function(er) {
        done(stream, er);
      });
    else
      done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.p2jcmd"></a>[module pdf2json.p2jcmd](#apidoc.module.pdf2json.p2jcmd)

#### <a name="apidoc.element.pdf2json.p2jcmd.p2jcmd"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>p2jcmd ()](#apidoc.element.pdf2json.p2jcmd.p2jcmd)
- description and source-code
```javascript
p2jcmd = function () {
    this.inputCount = 0;
    this.successCount = 0;
    this.failedCount = 0;
    this.warningCount = 0;

    this.p2j = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.p2jcmd.prototype"></a>[module pdf2json.p2jcmd.prototype](#apidoc.module.pdf2json.p2jcmd.prototype)

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.complete"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>complete (err)](#apidoc.element.pdf2json.p2jcmd.prototype.complete)
- description and source-code
```javascript
complete = function (err) {
    let statusMsg = "\n%d input files\t%d success\t%d fail\t%d warning.";
    console.log(statusMsg, this.inputCount, this.successCount, this.failedCount, this.warningCount);

    process.nextTick( () => {
        console.timeEnd(_PRO_TIMER);
        //let exitCode = (this.inputCount === this.successCount) ? 0 : 1;
        process.exit(0);
    });
}
```
- example usage
```shell
...

cls.prototype.processOneFile = function () {
    let inputDir = path.dirname(argv.f);
    let inputFile = path.basename(argv.f);

    this.inputCount = 1;
    this.p2j = new PDF2JSONUtil(inputDir, inputFile, this);
    this.p2j.processFile( data => this.complete(data) );
};

cls.prototype.processFiles = function(inputDir, files) {
    let fId = 0;
    this.p2j = new PDF2JSONUtil(inputDir, files[fId], this);
    this.p2j.processFile( function processPDFFile(err) {
        if (err) {
...
```

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.initialize"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>initialize ()](#apidoc.element.pdf2json.p2jcmd.prototype.initialize)
- description and source-code
```javascript
initialize = function (){
    console.time(_PRO_TIMER);
    let retVal = true;
    try {
        if (_.has(argv, 'v')) {
            console.log(pkInfo.version);
            retVal = false;
        }
        else if (_.has(argv, 'h')) {
            optimist.showHelp();
            retVal = false;
        }
        else if (!_.has(argv, 'f')) {
            optimist.showHelp();
            console.log("-f is required to specify input directory or file.");
            retVal = false;
        }
    }
    catch(e) {
        console.log("Exception: " + e.message);
        retVal = false;
    }
    return retVal;
}
```
- example usage
```shell
...
    console.log("Exception: " + e.message);
    retVal = false;
}
return retVal;
    };

    cls.prototype.start = function(){
if (!this.initialize()) {
    console.timeEnd(_PRO_TIMER);
    return;
}

try {
    console.log("\n" + _PRO_TIMER);
...
```

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.processFiles"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processFiles (inputDir, files)](#apidoc.element.pdf2json.p2jcmd.prototype.processFiles)
- description and source-code
```javascript
processFiles = function (inputDir, files) {
    let fId = 0;
    this.p2j = new PDF2JSONUtil(inputDir, files[fId], this);
    this.p2j.processFile( function processPDFFile(err) {
        if (err) {
            this.complete(err);
        }
        else {
            fId++;
            if (fId >= this.inputCount) {
                this.complete(null);
            }
            else {
                if (this.p2j) {
                    this.p2j.destroy();
                    this.p2j = null;
                }

                this.p2j = new PDF2JSONUtil(inputDir, files[fId], this);
                this.p2j.processFile(processPDFFile.bind(this));
            }
        }
    }.bind(this));
}
```
- example usage
```shell
...

    fs.readdir(inputDir, (err, files) => {
        let _iChars = "!@#$%^&*()+=[]\\\';,/{}|\":<>?~'.-_  ";
        let pdfFiles = files.filter( file => file.substr(-4).toLowerCase() === '.pdf' && _iChars.indexOf(file.substr(0,1)) < 0 );

        this.inputCount = pdfFiles.length;
        if (this.inputCount > 0) {
            this.processFiles(inputDir, pdfFiles);
        }
        else {
            console.log("No PDF files found. [" + inputDir + "].");
            this.complete(null);
        }
    });
};
...
```

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.processOneDirectory"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processOneDirectory ()](#apidoc.element.pdf2json.p2jcmd.prototype.processOneDirectory)
- description and source-code
```javascript
processOneDirectory = function () {
    let inputDir = path.normalize(argv.f);

    fs.readdir(inputDir, (err, files) => {
        let _iChars = "!@#$%^&*()+=[]\\\';,/{}|\":<>?~'.-_  ";
        let pdfFiles = files.filter( file => file.substr(-4).toLowerCase() === '.pdf' && _iChars.indexOf(file.substr(0,1)) < 0 );

        this.inputCount = pdfFiles.length;
        if (this.inputCount > 0) {
            this.processFiles(inputDir, pdfFiles);
        }
        else {
            console.log("No PDF files found. [" + inputDir + "].");
            this.complete(null);
        }
    });
}
```
- example usage
```shell
...

        let inputStatus = fs.statSync(argv.f);

        if (inputStatus.isFile()) {
            this.processOneFile();
        }
        else if (inputStatus.isDirectory()) {
            this.processOneDirectory();
        }
    }
    catch(e) {
        console.error("Exception: " + e.message);
        console.timeEnd(_PRO_TIMER);
    }
};
...
```

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.processOneFile"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>processOneFile ()](#apidoc.element.pdf2json.p2jcmd.prototype.processOneFile)
- description and source-code
```javascript
processOneFile = function () {
    let inputDir = path.dirname(argv.f);
    let inputFile = path.basename(argv.f);

    this.inputCount = 1;
    this.p2j = new PDF2JSONUtil(inputDir, inputFile, this);
    this.p2j.processFile( data => this.complete(data) );
}
```
- example usage
```shell
...

try {
    console.log("\n" + _PRO_TIMER);

    let inputStatus = fs.statSync(argv.f);

    if (inputStatus.isFile()) {
        this.processOneFile();
    }
    else if (inputStatus.isDirectory()) {
        this.processOneDirectory();
    }
}
catch(e) {
    console.error("Exception: " + e.message);
...
```

#### <a name="apidoc.element.pdf2json.p2jcmd.prototype.start"></a>[function <span class="apidocSignatureSpan">pdf2json.p2jcmd.prototype.</span>start ()](#apidoc.element.pdf2json.p2jcmd.prototype.start)
- description and source-code
```javascript
start = function (){
    if (!this.initialize()) {
        console.timeEnd(_PRO_TIMER);
        return;
    }

    try {
        console.log("\n" + _PRO_TIMER);

        let inputStatus = fs.statSync(argv.f);

        if (inputStatus.isFile()) {
            this.processOneFile();
        }
        else if (inputStatus.isDirectory()) {
            this.processOneDirectory();
        }
    }
    catch(e) {
        console.error("Exception: " + e.message);
        console.timeEnd(_PRO_TIMER);
    }
}
```
- example usage
```shell
...




'use strict';

var P2JCMD = require('./lib/p2jcmd');
new P2JCMD().start();
...
```



# <a name="apidoc.module.pdf2json.pdf"></a>[module pdf2json.pdf](#apidoc.module.pdf2json.pdf)

#### <a name="apidoc.element.pdf2json.pdf.pdf"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdf (needRawText)](#apidoc.element.pdf2json.pdf.pdf)
- description and source-code
```javascript
pdf = function (needRawText) {
    nodeEvents.EventEmitter.call(this);
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = () => _id;
    this.get_name = () => _name + _id;

    // public, this instance copies
    this.pdfDocument = null;
    this.pages = [];
    this.pageWidth = 0;
    this.rawTextContents = [];

    this.needRawText = needRawText;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdf.super_"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.</span>super_ ()](#apidoc.element.pdf2json.pdf.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdf.prototype"></a>[module pdf2json.pdf.prototype](#apidoc.module.pdf2json.pdf.prototype)

#### <a name="apidoc.element.pdf2json.pdf.prototype.destroy"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>destroy ()](#apidoc.element.pdf2json.pdf.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
    this.removeAllListeners();

    if (this.pdfDocument)
        this.pdfDocument.destroy();
    this.pdfDocument = null;

    this.pages = null;
    this.rawTextContents = null;
}
```
- example usage
```shell
...
    this.inputDir = null;
    this.inputFile = null;
    this.inputPath = null;
    this.outputDir = null;
    this.outputPath = null;

    if (this.pdfParser) {
        this.pdfParser.destroy();
    }
    this.pdfParser = null;
    this.curProcessor = null;
};

cls.prototype.processFile = function(callback) {
    let validateMsg = this.validateParams();
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.getAllFieldsTypes"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getAllFieldsTypes ()](#apidoc.element.pdf2json.pdf.prototype.getAllFieldsTypes)
- description and source-code
```javascript
getAllFieldsTypes = function () {
		return PDFField.getAllFieldsTypes({Pages:this.pages || [], Width: this.pageWidth});
	}
```
- example usage
```shell
...
    let fs = require('fs'),
        PDFParser = require("pdf2json");

    let pdfParser = new PDFParser();

    pdfParser.on("pdfParser_dataError", errData => console.error(errData.parserError) );
    pdfParser.on("pdfParser_dataReady", pdfData => {
        fs.writeFile("./pdf2json/test/F1040EZ.fields.json", JSON.stringify(pdfParser.getAllFieldsTypes()));
    });

    pdfParser.loadPDF("./pdf2json/test/pdf/fd/form/F1040EZ.pdf");
''''

Alternatively, you can pipe input and output streams: (requires v1.1.4)
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.getMergedTextBlocksIfNeeded"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getMergedTextBlocksIfNeeded ()](#apidoc.element.pdf2json.pdf.prototype.getMergedTextBlocksIfNeeded)
- description and source-code
```javascript
getMergedTextBlocksIfNeeded = function () {
		for (let p = 0; p < this.pages.length; p++) {
			let prevText = null;
			let page = this.pages[p];

			page.Texts.sort(PDFFont.compareBlockPos);
			page.Texts = page.Texts.filter( (t, j) => {
				let isDup = (j > 0) && PDFFont.areDuplicateBlocks(page.Texts[j-1], t);
				if (isDup) {
					nodeUtil.p2jinfo("skipped: dup text block: " + decodeURIComponent(t.R[0].T));
				}
				return !isDup;
			});

			for (let i = 0; i < page.Texts.length; i++) {
				let text = page.Texts[i];

				if (prevText) {
					if (PDFFont.areAdjacentBlocks(prevText, text) && PDFFont.haveSameStyle(prevText, text)) {
						let preT = decodeURIComponent(prevText.R[0].T);
						let curT = decodeURIComponent(text.R[0].T);

						prevText.R[0].T += text.R[0].T;
                        prevText.w += text.w;
                        text.merged = true;

						let mergedText = decodeURIComponent(prevText.R[0].T);
                        nodeUtil.p2jinfo('merged text block: ${preT} + ${curT} => ${mergedText}');
						prevText = null; //yeah, only merge two blocks for now
					}
					else {
						prevText = text;
					}
				}
				else {
					prevText = text;
				}
			}

			page.Texts = page.Texts.filter( t => !t.merged);
		}

		return {Pages:this.pages, Width: this.pageWidth};
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.getRawTextContent"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>getRawTextContent ()](#apidoc.element.pdf2json.pdf.prototype.getRawTextContent)
- description and source-code
```javascript
getRawTextContent = function () {
    let retVal = "";
    if (!this.needRawText)
        return retVal;

    _.each(this.rawTextContents, function(textContent, index) {
        let prevText = null;
        _.each(textContent.bidiTexts, function(textObj, idx) {
	            if (prevText) {
		            if (Math.abs(textObj.y - prevText.y) <= 9) {
			            prevText.str += textObj.str;
		            }
		            else {
			            retVal += prevText.str  + "\r\n";
			            prevText = textObj;
		            }
	            }
	            else {
		            prevText = textObj;
	            }

        });
	        if (prevText) {
		        retVal += prevText.str;
	        }
        retVal += "\r\n----------------Page (" + index + ") Break----------------\r\n";
    });

    return retVal;
}
```
- example usage
```shell
...
    let fs = require('fs'),
        PDFParser = require("pdf2json");

    let pdfParser = new PDFParser(this,1);

    pdfParser.on("pdfParser_dataError", errData => console.error(errData.parserError) );
    pdfParser.on("pdfParser_dataReady", pdfData => {
        fs.writeFile("./pdf2json/test/F1040EZ.content.txt", pdfParser.getRawTextContent());
    });

    pdfParser.loadPDF("./pdf2json/test/pdf/fd/form/F1040EZ.pdf");
''''

* Parse a PDF then write a fields.json file that only contains interactive forms' fields information:
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.load"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>load (pdfDocument, scale)](#apidoc.element.pdf2json.pdf.prototype.load)
- description and source-code
```javascript
load = function (pdfDocument, scale) {
    this.pdfDocument = pdfDocument;

	    return this.loadMetaData().then(
		    () => this.loadPages(),
			error => this.raiseErrorEvent("loadMetaData error: " + error)
	    );
}
```
- example usage
```shell
...


cls.prototype.parsePDFData = function(arrayBuffer) {
    this.pdfDocument = null;

    let parameters = {password: '', data: arrayBuffer};
    PDFJS.getDocument(parameters).then(
        pdfDocument => this.load(pdfDocument, 1),
        error => this.raiseErrorEvent("An error occurred while parsing the PDF: " + error)
    );
};

cls.prototype.tryLoadFieldInfoXML = function(pdfFilePath) {
    let fieldInfoXMLPath = pdfFilePath.replace(".pdf", _sufInfo);
    if ((fieldInfoXMLPath.indexOf(_sufInfo) < 1) || (!fs.existsSync(fieldInfoXMLPath))) {
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.loadMetaData"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>loadMetaData ()](#apidoc.element.pdf2json.pdf.prototype.loadMetaData)
- description and source-code
```javascript
loadMetaData = function () {
		return this.pdfDocument.getMetadata().then(
			data => {
				this.documentInfo = data.info;
				this.metadata = data.metadata;
				this.parseMetaData();
			},
			error => this.raiseErrorEvent("pdfDocument.getMetadata error: " + error)
		);
	}
```
- example usage
```shell
...
            }
        });
    };

    cls.prototype.load = function(pdfDocument, scale) {
        this.pdfDocument = pdfDocument;

	    return this.loadMetaData().then(
		    () => this.loadPages(),
			error => this.raiseErrorEvent("loadMetaData error: " + error)
	    );
    };

	cls.prototype.loadMetaData = function() {
		return this.pdfDocument.getMetadata().then(
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.loadPages"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>loadPages ()](#apidoc.element.pdf2json.pdf.prototype.loadPages)
- description and source-code
```javascript
loadPages = function () {
		let pagesCount = this.pdfDocument.numPages;
		let pagePromises = [];
		for (let i = 1; i <= pagesCount; i++)
			pagePromises.push(this.pdfDocument.getPage(i));

		let pagesPromise = PDFJS.Promise.all(pagePromises);

		nodeUtil.p2jinfo("PDF loaded. pagesCount = " + pagesCount);

		return pagesPromise.then(
			promisedPages => this.parsePage(promisedPages, 0, 1.5),
			error => this.raiseErrorEvent("pagesPromise error: " + error)
		);
	}
```
- example usage
```shell
...
        });
    };

    cls.prototype.load = function(pdfDocument, scale) {
        this.pdfDocument = pdfDocument;

	    return this.loadMetaData().then(
		    () => this.loadPages(),
			error => this.raiseErrorEvent("loadMetaData error: " + error)
	    );
    };

	cls.prototype.loadMetaData = function() {
		return this.pdfDocument.getMetadata().then(
			data => {
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.parseMetaData"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parseMetaData ()](#apidoc.element.pdf2json.pdf.prototype.parseMetaData)
- description and source-code
```javascript
parseMetaData = function () {
    let info = this.documentInfo;
    let metadata = this.metadata;

    let pdfTile = "";
    if (metadata && metadata.has('dc:title')) {
        pdfTile = metadata.get('dc:title');
    }
    else if (info && info['Title'])
        pdfTile = info['Title'];

    let formAttr = {AgencyId:"", Name: "", MC: false, Max: 1, Parent:""};
    if (metadata) {
        formAttr.AgencyId = _getMetaDataString(metadata, 'pdfx:agencyid');
        if (formAttr.AgencyId != "unknown")
            pdfTile = formAttr.AgencyId;

        formAttr.Name = _getMetaDataString(metadata, 'pdfx:name');
        formAttr.MC = _getMetaDataString(metadata, 'pdfx:mc') === 'true';
        formAttr.Max = _getMetaDataInt(metadata, 'pdfx:max');
        formAttr.Parent = _getMetaDataInt(metadata, 'pdfx:parent');
    }

    this.raiseReadyEvent({Transcoder: _PARSER_SIG, Agency:pdfTile, Id: formAttr});
}
```
- example usage
```shell
...
};

	cls.prototype.loadMetaData = function() {
		return this.pdfDocument.getMetadata().then(
			data => {
				this.documentInfo = data.info;
				this.metadata = data.metadata;
				this.parseMetaData();
			},
			error => this.raiseErrorEvent("pdfDocument.getMetadata error: " + error)
		);
	};

cls.prototype.parseMetaData = function() {
    let info = this.documentInfo;
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.parsePDFData"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parsePDFData (arrayBuffer)](#apidoc.element.pdf2json.pdf.prototype.parsePDFData)
- description and source-code
```javascript
parsePDFData = function (arrayBuffer) {
    this.pdfDocument = null;

    let parameters = {password: '', data: arrayBuffer};
    PDFJS.getDocument(parameters).then(
        pdfDocument => this.load(pdfDocument, 1),
        error => this.raiseErrorEvent("An error occurred while parsing the PDF: " + error)
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.parsePage"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>parsePage (promisedPages, id, scale)](#apidoc.element.pdf2json.pdf.prototype.parsePage)
- description and source-code
```javascript
parsePage = function (promisedPages, id, scale) {
    nodeUtil.p2jinfo("start to parse page:" + (id+1));

    let pdfPage = promisedPages[id];
    let pageParser = new PDFPageParser(pdfPage, id, scale, this.ptiParser);

    function continueOnNextPage() {
        nodeUtil.p2jinfo("complete parsing page:" + (id+1));
        if (id === (this.pdfDocument.numPages - 1) ) {
	            this.raiseReadyEvent({Pages:this.pages, Width: this.pageWidth});

	            //v1.1.2: signal end of parsed data with null
	            process.nextTick(() => this.raiseReadyEvent(null));
        }
        else {
            process.nextTick(() => this.parsePage(promisedPages, ++id, scale));
        }
    }

    pageParser.parsePage(
	        data => {
	            if (!this.pageWidth)  //get PDF width
	                this.pageWidth = pageParser.width;

	            let page = {Height: pageParser.height,
	                HLines: pageParser.HLines,
	                VLines: pageParser.VLines,
	                Fills:pageParser.Fills,
	//needs to keep current default output format, text content will output to a separate file if '-c' command line argument is set
	//                Content:pdfPage.getTextContent(),
	                Texts: pageParser.Texts,
	                Fields: pageParser.Fields,
	                Boxsets: pageParser.Boxsets
	            };

	            this.pages.push(page);

	            if (this.needRawText) {
	                pdfPage.getTextContent().then(
			            textContent => {
	                        this.rawTextContents.push(textContent);
	                        nodeUtil.p2jinfo("complete parsing raw text content:" + (id+1));
	                        continueOnNextPage.call(this);
	                    },
                    error => this.raiseErrorEvent("pdfPage.getTextContent error: " + error)
	                );
	            }
	            else {
		            continueOnNextPage.call(this);
	            }
	        },
	        errMsg => this.raiseErrorEvent("parsePage error:" + errMsg)
    );
}
```
- example usage
```shell
...
			pagePromises.push(this.pdfDocument.getPage(i));

		let pagesPromise = PDFJS.Promise.all(pagePromises);

		nodeUtil.p2jinfo("PDF loaded. pagesCount = " + pagesCount);

		return pagesPromise.then(
			promisedPages => this.parsePage(promisedPages, 0, 1.5),
			error => this.raiseErrorEvent("pagesPromise error: " + error)
		);
	};

cls.prototype.parsePage = function(promisedPages, id, scale) {
    nodeUtil.p2jinfo("start to parse page:" + (id+1));
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.raiseErrorEvent"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>raiseErrorEvent (errMsg)](#apidoc.element.pdf2json.pdf.prototype.raiseErrorEvent)
- description and source-code
```javascript
raiseErrorEvent = function (errMsg) {
    console.error(errMsg);
    process.nextTick( () => this.emit("pdfjs_parseDataError", errMsg));
    return errMsg;
}
```
- example usage
```shell
...

cls.prototype.parsePDFData = function(arrayBuffer) {
    this.pdfDocument = null;

    let parameters = {password: '', data: arrayBuffer};
    PDFJS.getDocument(parameters).then(
        pdfDocument => this.load(pdfDocument, 1),
        error => this.raiseErrorEvent("An error occurred while parsing the PDF: " + error)
    );
};

cls.prototype.tryLoadFieldInfoXML = function(pdfFilePath) {
    let fieldInfoXMLPath = pdfFilePath.replace(".pdf", _sufInfo);
    if ((fieldInfoXMLPath.indexOf(_sufInfo) < 1) || (!fs.existsSync(fieldInfoXMLPath))) {
        return;
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.raiseReadyEvent"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>raiseReadyEvent (data)](#apidoc.element.pdf2json.pdf.prototype.raiseReadyEvent)
- description and source-code
```javascript
raiseReadyEvent = function (data) {
    process.nextTick( () => this.emit("pdfjs_parseDataReady", data) );
    return data;
}
```
- example usage
```shell
...

            formAttr.Name = _getMetaDataString(metadata, 'pdfx:name');
            formAttr.MC = _getMetaDataString(metadata, 'pdfx:mc') === 'true';
            formAttr.Max = _getMetaDataInt(metadata, 'pdfx:max');
            formAttr.Parent = _getMetaDataInt(metadata, 'pdfx:parent');
        }

        this.raiseReadyEvent({Transcoder: _PARSER_SIG, Agency:pdfTile, Id: formAttr});
    };

	cls.prototype.loadPages = function() {
		let pagesCount = this.pdfDocument.numPages;
		let pagePromises = [];
		for (let i = 1; i <= pagesCount; i++)
			pagePromises.push(this.pdfDocument.getPage(i));
...
```

#### <a name="apidoc.element.pdf2json.pdf.prototype.tryLoadFieldInfoXML"></a>[function <span class="apidocSignatureSpan">pdf2json.pdf.prototype.</span>tryLoadFieldInfoXML (pdfFilePath)](#apidoc.element.pdf2json.pdf.prototype.tryLoadFieldInfoXML)
- description and source-code
```javascript
tryLoadFieldInfoXML = function (pdfFilePath) {
    let fieldInfoXMLPath = pdfFilePath.replace(".pdf", _sufInfo);
    if ((fieldInfoXMLPath.indexOf(_sufInfo) < 1) || (!fs.existsSync(fieldInfoXMLPath))) {
        return;
    }
    nodeUtil.p2jinfo("About to load fieldInfo XML : " + fieldInfoXMLPath);

    let PTIXmlParser = require('./ptixmlinject');
    this.ptiParser = new PTIXmlParser();
    this.ptiParser.parseXml(fieldInfoXMLPath, err => {
        if (err) {
            nodeUtil.p2jwarn("fieldInfo XML Error: " + JSON.stringify(err));
            this.ptiParser = null;
        }
        else {
            nodeUtil.p2jinfo("fieldInfo XML loaded.");
        }
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdfanno"></a>[module pdf2json.pdfanno](#apidoc.module.pdf2json.pdfanno)

#### <a name="apidoc.element.pdf2json.pdfanno.pdfanno"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfanno (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdfanno.pdfanno)
- description and source-code
```javascript
pdfanno = function (field, viewport, Fields, Boxsets) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function () {
        return _id;
    };
    this.get_name = function () {
        return _name + _id;
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfanno.processAnnotation"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfanno.</span>processAnnotation (annotation, item)](#apidoc.element.pdf2json.pdfanno.processAnnotation)
- description and source-code
```javascript
processAnnotation = function (annotation, item) {
    if (item.fieldType == 'Btn') { //PDF Spec p.675
        if (item.fieldFlags & 32768) {
            setupRadioButton(annotation, item);
        }
        else if (item.fieldFlags & 65536) {
            setupPushButton(annotation, item);
        }
        else {
            setupCheckBox(annotation, item);
        }
    }
    else if (item.fieldType == 'Ch') {
        setupDropDown(annotation, item);
    }
    else if (item.fieldType == 'Tx') {
        setupFieldAttributes(annotation, item);
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdfanno.prototype"></a>[module pdf2json.pdfanno.prototype](#apidoc.module.pdf2json.pdfanno.prototype)

#### <a name="apidoc.element.pdf2json.pdfanno.prototype.clean"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfanno.prototype.</span>clean ()](#apidoc.element.pdf2json.pdfanno.prototype.clean)
- description and source-code
```javascript
clean = function () {
    delete this.get_id;
    delete this.get_name;
}
```
- example usage
```shell
...
    console.warn("to be implemented: contextPrototype.measureText - ", text);
    let chars = text.length || 1;
    return {width: chars * (this.currentFont.spaceWidth || 5)};
};

contextPrototype.setFont = function(fontObj) {
    if ((!!this.currentFont) && _.isFunction(this.currentFont.clean)) {
        this.currentFont.clean();
        this.currentFont = null;
    }

    this.currentFont = new PDFFont(fontObj);
};

contextPrototype.clearRect = function () {
...
```



# <a name="apidoc.module.pdf2json.pdfcanvas"></a>[module pdf2json.pdfcanvas](#apidoc.module.pdf2json.pdfcanvas)

#### <a name="apidoc.element.pdf2json.pdfcanvas.pdfcanvas"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfcanvas (canvasTarget, scaledWidth, scaledHeight)](#apidoc.element.pdf2json.pdfcanvas.pdfcanvas)
- description and source-code
```javascript
function CanvasRenderingContext2D_(canvasTarget, scaledWidth, scaledHeight) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.m_ = createMatrixIdentity();

    this.mStack_ = [];
    this.aStack_ = [];
    this.currentPath_ = [];

    // Canvas context properties
    this.strokeStyle = '#000';
    this.fillStyle = '#000';

    this.lineWidth = 1;
    this.lineJoin = 'miter';
    this.lineCap = 'butt';
    this.dashArray = [];
    this.miterLimit = 1;
    this.globalAlpha = 1;

    if (!_.has(canvasTarget, "HLines") || !_.isArray(canvasTarget.HLines))
        canvasTarget.HLines = [];
    if (!_.has(canvasTarget, "VLines") || !_.isArray(canvasTarget.VLines))
        canvasTarget.VLines = [];
    if (!_.has(canvasTarget, "Fills") || !_.isArray(canvasTarget.Fills))
        canvasTarget.Fills = [];
    if (!_.has(canvasTarget, "Texts") || !_.isArray(canvasTarget.Texts))
        canvasTarget.Texts = [];

    this.canvas = canvasTarget;

    this.width = scaledWidth;
    this.height = scaledHeight;

    this.arcScaleX_ = 1;
    this.arcScaleY_ = 1;
    this.lineScale_ = 1;

    this.currentFont = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdfcanvas.prototype"></a>[module pdf2json.pdfcanvas.prototype](#apidoc.module.pdf2json.pdfcanvas.prototype)

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.arc"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>arc (aX, aY, aRadius, aStartAngle, aEndAngle, aClockwise)](#apidoc.element.pdf2json.pdfcanvas.prototype.arc)
- description and source-code
```javascript
arc = function (aX, aY, aRadius, aStartAngle, aEndAngle, aClockwise) {
    let arcType = aClockwise ? 'at' : 'wa';

    let xStart = aX + mc(aStartAngle) * aRadius;
    let yStart = aY + ms(aStartAngle) * aRadius;

    let xEnd = aX + mc(aEndAngle) * aRadius;
    let yEnd = aY + ms(aEndAngle) * aRadius;

    // IE won't render arches drawn counter clockwise if xStart == xEnd.
    if (xStart == xEnd && !aClockwise) {
        xStart += 0.125; // Offset xStart by 1/80 of a pixel. Use something
        // that can be represented in binary
    }

    let p = this.getCoords_(aX, aY);
    let pStart = this.getCoords_(xStart, yStart);
    let pEnd = this.getCoords_(xEnd, yEnd);

    this.currentPath_.push({type:arcType,
        x:p.x,
        y:p.y,
        radius:aRadius,
        xStart:pStart.x,
        yStart:pStart.y,
        xEnd:pEnd.x,
        yEnd:pEnd.y});

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.arcTo"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>arcTo ()](#apidoc.element.pdf2json.pdfcanvas.prototype.arcTo)
- description and source-code
```javascript
arcTo = function () {
    // TODO: Implement
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.beginPath"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>beginPath ()](#apidoc.element.pdf2json.pdfcanvas.prototype.beginPath)
- description and source-code
```javascript
beginPath = function () {
    // TODO: Branch current matrix so that save/restore has no effect
    //       as per safari docs.
    this.currentPath_ = [];
}
```
- example usage
```shell
...

    contextPrototype.strokeRect = function (aX, aY, aWidth, aHeight) {
if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
    return;//try to remove the rectangle behind radio buttons and checkboxes
}

let oldPath = this.currentPath_;
this.beginPath();

this.moveTo(aX, aY);
this.lineTo(aX + aWidth, aY);
this.lineTo(aX + aWidth, aY + aHeight);
this.lineTo(aX, aY + aHeight);
this.closePath();
this.stroke();
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.bezierCurveTo"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>bezierCurveTo (aCP1x, aCP1y, aCP2x, aCP2y, aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.bezierCurveTo)
- description and source-code
```javascript
bezierCurveTo = function (aCP1x, aCP1y, aCP2x, aCP2y, aX, aY) {
    let p = this.getCoords_(aX, aY);
    let cp1 = this.getCoords_(aCP1x, aCP1y);
    let cp2 = this.getCoords_(aCP2x, aCP2y);
    bezierCurveTo(this, cp1, cp2, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.clearRect"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>clearRect ()](#apidoc.element.pdf2json.pdfcanvas.prototype.clearRect)
- description and source-code
```javascript
clearRect = function () {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.clip"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>clip ()](#apidoc.element.pdf2json.pdfcanvas.prototype.clip)
- description and source-code
```javascript
clip = function () {
    // TODO: Implement
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.closePath"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>closePath ()](#apidoc.element.pdf2json.pdfcanvas.prototype.closePath)
- description and source-code
```javascript
closePath = function () {
    this.currentPath_.push({type:'close'});
}
```
- example usage
```shell
...
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
};

contextPrototype.strokeRect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.createLinearGradient"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createLinearGradient (aX0, aY0, aX1, aY1)](#apidoc.element.pdf2json.pdfcanvas.prototype.createLinearGradient)
- description and source-code
```javascript
createLinearGradient = function (aX0, aY0, aX1, aY1) {
    let gradient = new CanvasGradient_('gradient');
    gradient.x0_ = aX0;
    gradient.y0_ = aY0;
    gradient.x1_ = aX1;
    gradient.y1_ = aY1;
    return gradient;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.createPattern"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createPattern ()](#apidoc.element.pdf2json.pdfcanvas.prototype.createPattern)
- description and source-code
```javascript
createPattern = function () {
    return new CanvasPattern_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.createRadialGradient"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>createRadialGradient (aX0, aY0, aR0, aX1, aY1, aR1)](#apidoc.element.pdf2json.pdfcanvas.prototype.createRadialGradient)
- description and source-code
```javascript
createRadialGradient = function (aX0, aY0, aR0, aX1, aY1, aR1) {
    let gradient = new CanvasGradient_('gradientradial');
    gradient.x0_ = aX0;
    gradient.y0_ = aY0;
    gradient.r0_ = aR0;
    gradient.x1_ = aX1;
    gradient.y1_ = aY1;
    gradient.r1_ = aR1;
    return gradient;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.drawImage"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>drawImage (image, var_args)](#apidoc.element.pdf2json.pdfcanvas.prototype.drawImage)
- description and source-code
```javascript
drawImage = function (image, var_args) {
    //MQZ. no image drawing support for now
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.fill"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fill ()](#apidoc.element.pdf2json.pdfcanvas.prototype.fill)
- description and source-code
```javascript
fill = function () {
    this.stroke(true);
}
```
- example usage
```shell
...
    this.beginPath();

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
    this.fill();

    this.currentPath_ = oldPath;
};

contextPrototype.createLinearGradient = function (aX0, aY0, aX1, aY1) {
    let gradient = new CanvasGradient_('gradient');
    gradient.x0_ = aX0;
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.fillRect"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fillRect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.fillRect)
- description and source-code
```javascript
fillRect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    let oldPath = this.currentPath_;
    this.beginPath();

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
    this.fill();

    this.currentPath_ = oldPath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.fillText"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>fillText (text, x, y, maxWidth, fontSize)](#apidoc.element.pdf2json.pdfcanvas.prototype.fillText)
- description and source-code
```javascript
fillText = function (text, x, y, maxWidth, fontSize) {
    if (!text || text.trim().length < 1)
        return;
    let p = this.getCoords_(x, y);

    let a = processStyle(this.fillStyle || this.strokeStyle);
    let color = (!!a) ? a.color : '#000000';

    this.currentFont.processText(p, text, maxWidth, color, fontSize, this.canvas, this.m_);
}
```
- example usage
```shell
...
    let color = (!!a) ? a.color : '#000000';

    this.currentFont.processText(p, text, maxWidth, color, fontSize, this.canvas, this.m_);
};

contextPrototype.strokeText = function(text, x, y, maxWidth) {
    //MQZ. 10/23/2012, yeah, no hollow text for now
    this.fillText(text, x, y, maxWidth);
};

contextPrototype.measureText = function(text) {
    console.warn("to be implemented: contextPrototype.measureText - ", text);
    let chars = text.length || 1;
    return {width: chars * (this.currentFont.spaceWidth || 5)};
};
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.getContext"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getContext (ctxType)](#apidoc.element.pdf2json.pdfcanvas.prototype.getContext)
- description and source-code
```javascript
getContext = function (ctxType) {
    return (ctxType === "2d") ? this : null;
}
```
- example usage
```shell
...
    cls.prototype.parsePage = function(callback, errorCallBack) {
        if (this.renderingState !== RenderingStates.INITIAL)
          error('Must be in new state before drawing');

        this.renderingState = RenderingStates.RUNNING;

        let canvas = createScratchCanvas(1, 1);
        let ctx = canvas.getContext('2d');

        function pageViewDrawCallback(error) {
this.renderingState = RenderingStates.FINISHED;

if (error) {
    let errMsg = 'An error occurred while rendering the page ' + (this.id + 1) +
        ':\n' + error.message +
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.getCoords_"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getCoords_ (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.getCoords_)
- description and source-code
```javascript
getCoords_ = function (aX, aY) {
    let m = this.m_;
    return {
        x: (aX * m[0][0] + aY * m[1][0] + m[2][0]),
        y: (aX * m[0][1] + aY * m[1][1] + m[2][1])
    };
}
```
- example usage
```shell
...
contextPrototype.getLineDash= function() {
    return this.dashArray;
};

contextPrototype.fillText = function(text, x, y, maxWidth, fontSize) {
    if (!text || text.trim().length < 1)
        return;
    let p = this.getCoords_(x, y);

    let a = processStyle(this.fillStyle || this.strokeStyle);
    let color = (!!a) ? a.color : '#000000';

    this.currentFont.processText(p, text, maxWidth, color, fontSize, this.canvas, this.m_);
};
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.getImageData"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getImageData (x, y, w, h)](#apidoc.element.pdf2json.pdfcanvas.prototype.getImageData)
- description and source-code
```javascript
getImageData = function (x, y, w, h) {
    //MQZ. returns empty data buffer for now
    return {
        width:w,
        height:h,
        data:new Uint8Array(w * h * 4)
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.getLineDash"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>getLineDash ()](#apidoc.element.pdf2json.pdfcanvas.prototype.getLineDash)
- description and source-code
```javascript
getLineDash = function () {
    return this.dashArray;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.lineTo"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>lineTo (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.lineTo)
- description and source-code
```javascript
lineTo = function (aX, aY) {
    let p = this.getCoords_(aX, aY);
    this.currentPath_.push({type:'lineTo', x:p.x, y:p.y});

    this.currentX_ = p.x;
    this.currentY_ = p.y;
}
```
- example usage
```shell
...

contextPrototype.rect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
};

contextPrototype.strokeRect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.measureText"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>measureText (text)](#apidoc.element.pdf2json.pdfcanvas.prototype.measureText)
- description and source-code
```javascript
measureText = function (text) {
    console.warn("to be implemented: contextPrototype.measureText - ", text);
    let chars = text.length || 1;
    return {width: chars * (this.currentFont.spaceWidth || 5)};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.moveTo"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>moveTo (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.moveTo)
- description and source-code
```javascript
moveTo = function (aX, aY) {
    let p = this.getCoords_(aX, aY);
    this.currentPath_.push({type:'moveTo', x:p.x, y:p.y});
    this.currentX_ = p.x;
    this.currentY_ = p.y;
}
```
- example usage
```shell
...
};

contextPrototype.rect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
};

contextPrototype.strokeRect = function (aX, aY, aWidth, aHeight) {
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.quadraticCurveTo"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>quadraticCurveTo (aCPx, aCPy, aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.quadraticCurveTo)
- description and source-code
```javascript
quadraticCurveTo = function (aCPx, aCPy, aX, aY) {
    // the following is lifted almost directly from
    // http://developer.mozilla.org/en/docs/Canvas_tutorial:Drawing_shapes

    let cp = this.getCoords_(aCPx, aCPy);
    let p = this.getCoords_(aX, aY);

    let cp1 = {
        x:this.currentX_ + 2.0 / 3.0 * (cp.x - this.currentX_),
        y:this.currentY_ + 2.0 / 3.0 * (cp.y - this.currentY_)
    };
    let cp2 = {
        x:cp1.x + (p.x - this.currentX_) / 3.0,
        y:cp1.y + (p.y - this.currentY_) / 3.0
    };

    bezierCurveTo(this, cp1, cp2, p);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.rect"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>rect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.rect)
- description and source-code
```javascript
rect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.restore"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>restore ()](#apidoc.element.pdf2json.pdfcanvas.prototype.restore)
- description and source-code
```javascript
restore = function () {
    copyState(this.aStack_.pop(), this);
    this.m_ = this.mStack_.pop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.rotate"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>rotate (aRot)](#apidoc.element.pdf2json.pdfcanvas.prototype.rotate)
- description and source-code
```javascript
rotate = function (aRot) {
    let c = mc(aRot);
    let s = ms(aRot);

    let m1 = [
        [c, s, 0],
        [-s, c, 0],
        [0, 0, 1]
    ];

    setM(this, matrixMultiply(m1, this.m_), false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.save"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>save ()](#apidoc.element.pdf2json.pdfcanvas.prototype.save)
- description and source-code
```javascript
save = function () {
    let o = {};
    copyState(this, o);
    this.aStack_.push(o);
    this.mStack_.push(this.m_);
    this.m_ = matrixMultiply(createMatrixIdentity(), this.m_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.scale"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>scale (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.scale)
- description and source-code
```javascript
scale = function (aX, aY) {
    this.arcScaleX_ *= aX;
    this.arcScaleY_ *= aY;
    let m1 = [
        [aX, 0, 0],
        [0, aY, 0],
        [0, 0, 1]
    ];

    setM(this, matrixMultiply(m1, this.m_), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.setFont"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setFont (fontObj)](#apidoc.element.pdf2json.pdfcanvas.prototype.setFont)
- description and source-code
```javascript
setFont = function (fontObj) {
    if ((!!this.currentFont) && _.isFunction(this.currentFont.clean)) {
        this.currentFont.clean();
        this.currentFont = null;
    }

    this.currentFont = new PDFFont(fontObj);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.setLineDash"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setLineDash (lineDash)](#apidoc.element.pdf2json.pdfcanvas.prototype.setLineDash)
- description and source-code
```javascript
setLineDash = function (lineDash) {
    this.dashArray = lineDash;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.setTransform"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>setTransform (m11, m12, m21, m22, dx, dy)](#apidoc.element.pdf2json.pdfcanvas.prototype.setTransform)
- description and source-code
```javascript
setTransform = function (m11, m12, m21, m22, dx, dy) {
    let m = [
        [m11, m12, 0],
        [m21, m22, 0],
        [dx, dy, 1]
    ];

    setM(this, m, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.stroke"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>stroke (aFill)](#apidoc.element.pdf2json.pdfcanvas.prototype.stroke)
- description and source-code
```javascript
stroke = function (aFill) {
    if (this.currentPath_.length < 2) {
        return;
    }

    let a = processStyle(aFill ? this.fillStyle : this.strokeStyle);
    let color = a.color;
//        let opacity = a.alpha * this.globalAlpha;
    let lineWidth = this.lineScale_ * this.lineWidth;

    let min = {x:null, y:null};
    let max = {x:null, y:null};

    for (let i = 0; i < this.currentPath_.length; i++) {
        let p = this.currentPath_[i];

        switch (p.type) {
            case 'moveTo':
                break;
            case 'lineTo':
                if (!aFill) { //lines
                    if (i > 0) {
                        _drawPDFLine.call(this, this.currentPath_[i-1], p, lineWidth, color);
                    }
                }
                break;
            case 'close':
                if (!aFill) { //lines
                    if (i > 0) {
                        _drawPDFLine.call(this, this.currentPath_[i-1], this.currentPath_[0], lineWidth, color);
                    }
                }
                p = null;
                break;
            case 'bezierCurveTo':
                break;
            case 'at':
            case 'wa':
                break;
        }

        // Figure out dimensions so we can set fills' coordinates correctly
        if (aFill && p) {
            if (min.x == null || p.x < min.x) {
                min.x = p.x;
            }
            if (max.x == null || p.x > max.x) {
                max.x = p.x;
            }
            if (min.y == null || p.y < min.y) {
                min.y = p.y;
            }
            if (max.y == null || p.y > max.y) {
                max.y = p.y;
            }
        }
    }

    if (aFill) { //fill
        _drawPDFFill.call(this, min, min, max, color);
    }
}
```
- example usage
```shell
...
    this.beginPath();

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
    this.stroke();

    this.currentPath_ = oldPath;
};

contextPrototype.fillRect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
...
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.strokeRect"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>strokeRect (aX, aY, aWidth, aHeight)](#apidoc.element.pdf2json.pdfcanvas.prototype.strokeRect)
- description and source-code
```javascript
strokeRect = function (aX, aY, aWidth, aHeight) {
    if (_needRemoveRect.call(this, aX, aY, aWidth, aHeight)) {
        return;//try to remove the rectangle behind radio buttons and checkboxes
    }

    let oldPath = this.currentPath_;
    this.beginPath();

    this.moveTo(aX, aY);
    this.lineTo(aX + aWidth, aY);
    this.lineTo(aX + aWidth, aY + aHeight);
    this.lineTo(aX, aY + aHeight);
    this.closePath();
    this.stroke();

    this.currentPath_ = oldPath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.strokeText"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>strokeText (text, x, y, maxWidth)](#apidoc.element.pdf2json.pdfcanvas.prototype.strokeText)
- description and source-code
```javascript
strokeText = function (text, x, y, maxWidth) {
    //MQZ. 10/23/2012, yeah, no hollow text for now
    this.fillText(text, x, y, maxWidth);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.transform"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>transform (m11, m12, m21, m22, dx, dy)](#apidoc.element.pdf2json.pdfcanvas.prototype.transform)
- description and source-code
```javascript
transform = function (m11, m12, m21, m22, dx, dy) {
    let m1 = [
        [m11, m12, 0],
        [m21, m22, 0],
        [dx, dy, 1]
    ];

    setM(this, matrixMultiply(m1, this.m_), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfcanvas.prototype.translate"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfcanvas.prototype.</span>translate (aX, aY)](#apidoc.element.pdf2json.pdfcanvas.prototype.translate)
- description and source-code
```javascript
translate = function (aX, aY) {
    let m1 = [
        [1, 0, 0],
        [0, 1, 0],
        [aX, aY, 1]
    ];

    setM(this, matrixMultiply(m1, this.m_), false);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdffield"></a>[module pdf2json.pdffield](#apidoc.module.pdf2json.pdffield)

#### <a name="apidoc.element.pdf2json.pdffield.pdffield"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffield (field, viewport, Fields, Boxsets)](#apidoc.element.pdf2json.pdffield.pdffield)
- description and source-code
```javascript
pdffield = function (field, viewport, Fields, Boxsets) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.field = field;
    this.viewport = viewport;
    this.Fields = Fields;
    this.Boxsets = Boxsets;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffield.getAllFieldsTypes"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>getAllFieldsTypes (data)](#apidoc.element.pdf2json.pdffield.getAllFieldsTypes)
- description and source-code
```javascript
getAllFieldsTypes = function (data) {

    function isFieldReadOnly(field) {
        return (field.AM & kFBANotOverridable) ? true : false;
    }

    function getFieldBase(field) {
        return {id: field.id.Id, type: field.T.Name, calc: isFieldReadOnly(field), value: field.V || ""};
    }

    let retVal = [];

    _.each(data.Pages, function(page) {
        _.each(page.Boxsets, function(boxsets) {
            if (boxsets.boxes.length > 1) { //radio button
                _.each(boxsets.boxes, function(box) {
                    retVal.push({id: boxsets.id.Id, type: "radio", calc: isFieldReadOnly(box), value: box.id.Id});
                });
            }
            else { //checkbox
                retVal.push(getFieldBase(boxsets.boxes[0]));
            }
        });

        _.each(page.Fields, function(field){
            retVal.push(getFieldBase(field));
        });
    });
    return retVal;
}
```
- example usage
```shell
...
    let fs = require('fs'),
        PDFParser = require("pdf2json");

    let pdfParser = new PDFParser();

    pdfParser.on("pdfParser_dataError", errData => console.error(errData.parserError) );
    pdfParser.on("pdfParser_dataReady", pdfData => {
        fs.writeFile("./pdf2json/test/F1040EZ.fields.json", JSON.stringify(pdfParser.getAllFieldsTypes()));
    });

    pdfParser.loadPDF("./pdf2json/test/pdf/fd/form/F1040EZ.pdf");
''''

Alternatively, you can pipe input and output streams: (requires v1.1.4)
...
```

#### <a name="apidoc.element.pdf2json.pdffield.isFormElement"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>isFormElement (field)](#apidoc.element.pdf2json.pdffield.isFormElement)
- description and source-code
```javascript
isFormElement = function (field) {
    let retVal = false;
    switch(field.subtype) {
        case 'Widget': retVal = cls.isWidgetSupported(field); break;
        default:
            nodeUtil.p2jwarn("Unsupported: field.type of " + field.subtype);
            break;
    }
    return retVal;
}
```
- example usage
```shell
...
  INITIAL: 0,
  RUNNING: 1,
  PAUSED: 2,
  FINISHED: 3
};

let _addField = function(field) {
    if (!PDFField.isFormElement(field))
        return;

    let oneField = new PDFField(field, this.viewport, this.Fields, this.Boxsets);
    oneField.processField();
};

// constructor
...
```

#### <a name="apidoc.element.pdf2json.pdffield.isWidgetSupported"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffield.</span>isWidgetSupported (field)](#apidoc.element.pdf2json.pdffield.isWidgetSupported)
- description and source-code
```javascript
isWidgetSupported = function (field) {
    let retVal = false;

    switch(field.fieldType) {
        case 'Tx': retVal = true; break; //text input
        case 'Btn':
            if (field.fieldFlags & 32768) {
                field.fieldType = 'Rd'; //radio button
            }
            else if (field.fieldFlags & 65536) {
                field.fieldType = 'Btn'; //push button
            }
            else {
                field.fieldType = 'Cb'; //checkbox
            }
            retVal = true;
            break;
        case 'Ch': retVal = true; break; //drop down
        default:
            nodeUtil.p2jwarn("Unsupported: field.fieldType of " + field.fieldType);
            break;
    }

    return retVal;
}
```
- example usage
```shell
...

    return retVal;
};

cls.isFormElement = function(field) {
    let retVal = false;
    switch(field.subtype) {
        case 'Widget': retVal = cls.isWidgetSupported(field); break;
        default:
            nodeUtil.p2jwarn("Unsupported: field.type of " + field.subtype);
            break;
    }
    return retVal;
};
...
```



# <a name="apidoc.module.pdf2json.pdffield.prototype"></a>[module pdf2json.pdffield.prototype](#apidoc.module.pdf2json.pdffield.prototype)

#### <a name="apidoc.element.pdf2json.pdffield.prototype.clean"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffield.prototype.</span>clean ()](#apidoc.element.pdf2json.pdffield.prototype.clean)
- description and source-code
```javascript
clean = function () {
    delete this.get_id;
    delete this.get_name;

    delete this.field;
    delete this.viewport;
    delete this.Fields;
    delete this.Boxsets;
}
```
- example usage
```shell
...
    console.warn("to be implemented: contextPrototype.measureText - ", text);
    let chars = text.length || 1;
    return {width: chars * (this.currentFont.spaceWidth || 5)};
};

contextPrototype.setFont = function(fontObj) {
    if ((!!this.currentFont) && _.isFunction(this.currentFont.clean)) {
        this.currentFont.clean();
        this.currentFont = null;
    }

    this.currentFont = new PDFFont(fontObj);
};

contextPrototype.clearRect = function () {
...
```

#### <a name="apidoc.element.pdf2json.pdffield.prototype.processField"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffield.prototype.</span>processField ()](#apidoc.element.pdf2json.pdffield.prototype.processField)
- description and source-code
```javascript
processField = function () {

    this.field.TI = _tabIndex++;

    switch(this.field.fieldType) {
        case 'Tx': _addAlpha.call(this, this.field); break;
        case 'Cb': _addCheckBox.call(this, this.field); break;
        case 'Rd': _addRadioButton.call(this, this.field);break;
        case 'Btn':_addLinkButton.call(this, this.field); break;
        case 'Ch': _addSelect.call(this, this.field); break;
    }

    this.clean();
}
```
- example usage
```shell
...
};

let _addField = function(field) {
    if (!PDFField.isFormElement(field))
        return;

    let oneField = new PDFField(field, this.viewport, this.Fields, this.Boxsets);
    oneField.processField();
};

// constructor
let cls = function (pdfPage, id, scale, ptiParser) {
    nodeEvents.EventEmitter.call(this);
    // private
    let _id = _nextId++;
...
```



# <a name="apidoc.module.pdf2json.pdffill"></a>[module pdf2json.pdffill](#apidoc.module.pdf2json.pdffill)

#### <a name="apidoc.element.pdf2json.pdffill.pdffill"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffill (x, y, width, height, color)](#apidoc.element.pdf2json.pdffill.pdffill)
- description and source-code
```javascript
pdffill = function (x, y, width, height, color) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.x = x;
    this.y = y;
    this.width = width;
    this.height = height;
    this.color = color;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdffill.prototype"></a>[module pdf2json.pdffill.prototype](#apidoc.module.pdf2json.pdffill.prototype)

#### <a name="apidoc.element.pdf2json.pdffill.prototype.processFill"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffill.prototype.</span>processFill (targetData)](#apidoc.element.pdf2json.pdffill.prototype.processFill)
- description and source-code
```javascript
processFill = function (targetData) {
    let clrId = PDFUnit.findColorIndex(this.color);

    let oneFill = {x:PDFUnit.toFormX(this.x),
                   y:PDFUnit.toFormY(this.y),
                   w:PDFUnit.toFormX(this.width),
                   h:PDFUnit.toFormY(this.height),
                   clr: clrId};

    //MQZ.07/29/2013: when color is not in color dictionary, set the original color (oc)
    if (clrId < 0) {
        oneFill = _.extend({oc: this.color}, oneFill);
    }

    targetData.Fills.push(oneFill);
}
```
- example usage
```shell
...
    pL.processLine(this.canvas);
};

let _drawPDFFill = function(cp, min, max, color) {
    let width = max.x - min.x;
    let height = max.y - min.y;
    let pF = new PDFFill(cp.x, cp.y, width, height, color);
    pF.processFill(this.canvas);
};

let _needRemoveRect = function(x, y, w, h) {
    let retVal = (Math.abs(w - Math.abs(h)) < 1 && w < 13);
    if (retVal) {
        nodeUtil.p2jinfo("Skipped: tiny rect: w=" + w + ", h=" + h);
    }
...
```



# <a name="apidoc.module.pdf2json.pdffont"></a>[module pdf2json.pdffont](#apidoc.module.pdf2json.pdffont)

#### <a name="apidoc.element.pdf2json.pdffont.pdffont"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdffont (fontObj)](#apidoc.element.pdf2json.pdffont.pdffont)
- description and source-code
```javascript
pdffont = function (fontObj) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.fontObj = fontObj;
    let typeName = (fontObj.name || fontObj.fallbackName);
    if (!typeName) {
        typeName = _kFontFaces[0]; //default font family name
    }
    typeName = typeName.toLowerCase();
    this.typeName = typeName;

    let subType = typeName;
    let nameArray = typeName.split('+');
    if (_.isArray(nameArray) && nameArray.length > 1) {
        subType = nameArray[1].split("-");
        if (_.isArray(subType) && subType.length > 1) {
            if (!this.bold) {
                let subName = subType[1].toLowerCase();
                this.bold = _boldSubNames.indexOf(subName) >= 0;
            }
            subType = subType[0];
        }
    }
    this.subType = subType;

    this.isSymbol = typeName.indexOf("symbol") > 0 || _kFontFaces[2].indexOf(this.subType) >= 0;
    if (this.fontObj.isSymbolicFont) {
        let mFonts = _stdFonts.filter( (oneName) => (typeName.indexOf(oneName) >= 0) );

        if (mFonts.length > 0) {
            this.fontObj.isSymbolicFont = false; //lots of Arial-based font is detected as symbol in VA forms (301, 76-c, etc.)
reset the flag for now
            nodeUtil.p2jinfo("Reset: isSymbolicFont (false) for " + this.fontObj.name);
        }
    }
    else {
        if (this.isSymbol) {
            this.fontObj.isSymbolicFont = true; //text pdf: va_ind_760c
            nodeUtil.p2jinfo("Reset: isSymbolicFont (true) for " + this.fontObj.name);
        }
    }

    this.fontSize = 1;

    this.faceIdx = 0;
    this.bold = false;
    this.italic = false;

    this.fontStyleId = -1;

	    this.spaceWidth = fontObj.spaceWidth;
	    if (!this.spaceWidth) {
		    var spaceId = Array.isArray(fontObj.toFontChar) ? fontObj.toFontChar.indexOf(32) : -1;
		    this.spaceWidth = (spaceId >= 0 && Array.isArray(fontObj.widths)) ? fontObj.widths[spaceId] : 250;
	    }
	    this.spaceWidth = PDFUnit.toFormX(this.spaceWidth) / 32;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffont.areAdjacentBlocks"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>areAdjacentBlocks (t1, t2)](#apidoc.element.pdf2json.pdffont.areAdjacentBlocks)
- description and source-code
```javascript
areAdjacentBlocks = function (t1, t2) {
    let isInSameLine = Math.abs(t1.y - t2.y) <= DISTANCE_DELTA;
    let isDistanceSmallerThanASpace = ((t2.x - t1.x - t1.w) < cls.getSpaceThreshHold(t1));

    return isInSameLine && isDistanceSmallerThanASpace;
}
```
- example usage
```shell
...
				return !isDup;
			});

			for (let i = 0; i < page.Texts.length; i++) {
				let text = page.Texts[i];

				if (prevText) {
					if (PDFFont.areAdjacentBlocks(prevText, text) && PDFFont.haveSameStyle(prevText, text)) {
						let preT = decodeURIComponent(prevText.R[0].T);
						let curT = decodeURIComponent(text.R[0].T);

						prevText.R[0].T += text.R[0].T;
prevText.w += text.w;
text.merged = true;
...
```

#### <a name="apidoc.element.pdf2json.pdffont.areDuplicateBlocks"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>areDuplicateBlocks (t1, t2)](#apidoc.element.pdf2json.pdffont.areDuplicateBlocks)
- description and source-code
```javascript
areDuplicateBlocks = function (t1, t2) {
    return t1.x == t2.x && t1.y == t2.y && t1.R[0].T == t2.R[0].T && cls.haveSameStyle(t1, t2);
}
```
- example usage
```shell
...
	cls.prototype.getMergedTextBlocksIfNeeded = function() {
		for (let p = 0; p < this.pages.length; p++) {
			let prevText = null;
			let page = this.pages[p];

			page.Texts.sort(PDFFont.compareBlockPos);
			page.Texts = page.Texts.filter( (t, j) => {
				let isDup = (j > 0) && PDFFont.areDuplicateBlocks(page.Texts[j-1], t);
				if (isDup) {
					nodeUtil.p2jinfo("skipped: dup text block: " + decodeURIComponent(t.R[0].T));
				}
				return !isDup;
			});

			for (let i = 0; i < page.Texts.length; i++) {
...
```

#### <a name="apidoc.element.pdf2json.pdffont.compareBlockPos"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>compareBlockPos (t1, t2)](#apidoc.element.pdf2json.pdffont.compareBlockPos)
- description and source-code
```javascript
compareBlockPos = function (t1, t2) {
    if (t1.y < t2.y - DISTANCE_DELTA) {
        return -1;
    }
    if (Math.abs(t1.y - t2.y) <= DISTANCE_DELTA) {
        if (t1.x < t2.x - DISTANCE_DELTA) {
            return -1;
        }
        if (Math.abs(t1.x - t2.x) <= DISTANCE_DELTA) {
            return 0;
        }
    }
    return 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdffont.getFontSize"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>getFontSize (textBlock)](#apidoc.element.pdf2json.pdffont.getFontSize)
- description and source-code
```javascript
getFontSize = function (textBlock) {
		let sId = textBlock.R[0].S;
		return (sId < 0) ? textBlock.R[0].TS[1] : _kFontStyles[sId][1];
	}
```
- example usage
```shell
...
    retVal = (typeof t1.R[0].RA === 'undefined') && (typeof t2.R[0].RA === 'undefined');
}

return retVal;
    };

    cls.getSpaceThreshHold = function(t1) {
return (PDFFont.getFontSize(t1)/12) * t1.sw;
    };

    cls.areAdjacentBlocks = function(t1, t2) {
let isInSameLine = Math.abs(t1.y - t2.y) <= DISTANCE_DELTA;
let isDistanceSmallerThanASpace = ((t2.x - t1.x - t1.w) < cls.getSpaceThreshHold(t1));

return isInSameLine && isDistanceSmallerThanASpace;
...
```

#### <a name="apidoc.element.pdf2json.pdffont.getSpaceThreshHold"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>getSpaceThreshHold (t1)](#apidoc.element.pdf2json.pdffont.getSpaceThreshHold)
- description and source-code
```javascript
getSpaceThreshHold = function (t1) {
    return (PDFFont.getFontSize(t1)/12) * t1.sw;
}
```
- example usage
```shell
...

    cls.getSpaceThreshHold = function(t1) {
        return (PDFFont.getFontSize(t1)/12) * t1.sw;
    };

    cls.areAdjacentBlocks = function(t1, t2) {
        let isInSameLine = Math.abs(t1.y - t2.y) <= DISTANCE_DELTA;
        let isDistanceSmallerThanASpace = ((t2.x - t1.x - t1.w) < cls.getSpaceThreshHold(t1));

        return isInSameLine && isDistanceSmallerThanASpace;
    };

	cls.getFontSize = function(textBlock) {
		let sId = textBlock.R[0].S;
		return (sId < 0) ? textBlock.R[0].TS[1] : _kFontStyles[sId][1];
...
```

#### <a name="apidoc.element.pdf2json.pdffont.haveSameStyle"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.</span>haveSameStyle (t1, t2)](#apidoc.element.pdf2json.pdffont.haveSameStyle)
- description and source-code
```javascript
haveSameStyle = function (t1, t2) {
    let retVal = t1.R[0].S === t2.R[0].S;
    if (retVal && t1.R[0].S < 0) {
        for (let i = 0; i < t1.R[0].TS.length; i++) {
            if (t1.R[0].TS[i] !== t2.R[0].TS[i]) {
                retVal = false;
                break;
            }
        }
    }
    if (retVal) { // make sure both block are not rotated
        retVal = (typeof t1.R[0].RA === 'undefined') && (typeof t2.R[0].RA === 'undefined');
    }

    return retVal;
}
```
- example usage
```shell
...
				return !isDup;
			});

			for (let i = 0; i < page.Texts.length; i++) {
				let text = page.Texts[i];

				if (prevText) {
					if (PDFFont.areAdjacentBlocks(prevText, text) && PDFFont.haveSameStyle(prevText, text)) {
						let preT = decodeURIComponent(prevText.R[0].T);
						let curT = decodeURIComponent(text.R[0].T);

						prevText.R[0].T += text.R[0].T;
prevText.w += text.w;
text.merged = true;
...
```



# <a name="apidoc.module.pdf2json.pdffont.prototype"></a>[module pdf2json.pdffont.prototype](#apidoc.module.pdf2json.pdffont.prototype)

#### <a name="apidoc.element.pdf2json.pdffont.prototype.clean"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>clean ()](#apidoc.element.pdf2json.pdffont.prototype.clean)
- description and source-code
```javascript
clean = function () {
    this.fontObj = null;
    delete this.fontObj;
}
```
- example usage
```shell
...
    console.warn("to be implemented: contextPrototype.measureText - ", text);
    let chars = text.length || 1;
    return {width: chars * (this.currentFont.spaceWidth || 5)};
};

contextPrototype.setFont = function(fontObj) {
    if ((!!this.currentFont) && _.isFunction(this.currentFont.clean)) {
        this.currentFont.clean();
        this.currentFont = null;
    }

    this.currentFont = new PDFFont(fontObj);
};

contextPrototype.clearRect = function () {
...
```

#### <a name="apidoc.element.pdf2json.pdffont.prototype.flash_encode"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>flash_encode (str)](#apidoc.element.pdf2json.pdffont.prototype.flash_encode)
- description and source-code
```javascript
flash_encode = function (str) {
    let retVal = encodeURIComponent(str);
    retVal = retVal.replace("%C2%96", "-");
    retVal = retVal.replace("%C2%91", "%27");
    retVal = retVal.replace("%C2%92", "%27");
    retVal = retVal.replace("%C2%82", "%27");
    retVal = retVal.replace("%C2%93", "%22");
    retVal = retVal.replace("%C2%94", "%22");
    retVal = retVal.replace("%C2%84", "%22");
    retVal = retVal.replace("%C2%8B", "%C2%AB");
    retVal = retVal.replace("%C2%9B", "%C2%BB");

    return retVal;
}
```
- example usage
```shell
...
let oneText = {x: PDFUnit.toFormX(p.x) - 0.25,
    y: PDFUnit.toFormY(p.y) - 0.75,
    w: PDFUnit.toFixedFloat(maxWidth),
	        sw: this.spaceWidth, //font space width, use to merge adjacent text blocks
    clr: clrId,
    A: "left",
    R: [{
        T: this.flash_encode(text),
        S: this.fontStyleId,
        TS: TS
    }]
};

//MQZ.07/29/2013: when color is not in color dictionary, set the original color (oc)
if (clrId < 0) {
...
```

#### <a name="apidoc.element.pdf2json.pdffont.prototype.processText"></a>[function <span class="apidocSignatureSpan">pdf2json.pdffont.prototype.</span>processText (p, str, maxWidth, color, fontSize, targetData, matrix2D)](#apidoc.element.pdf2json.pdffont.prototype.processText)
- description and source-code
```javascript
processText = function (p, str, maxWidth, color, fontSize, targetData, matrix2D) {
    let text = _processSymbolicFont.call(this, str);
    if (!text) {
        return;
    }
    this.fontStyleId = _getFontStyleIndex.call(this, fontSize);

    // when this.fontStyleId === -1, it means the text style doesn't match any entry in the dictionary
    // adding TS to better describe text style [fontFaceId, fontSize, 1/0 for bold, 1/0 for italic];
    let TS = [this.faceIdx, this.fontSize, this.bold?1:0, this.italic?1:0];

    let clrId = PDFUnit.findColorIndex(color);

    let oneText = {x: PDFUnit.toFormX(p.x) - 0.25,
        y: PDFUnit.toFormY(p.y) - 0.75,
        w: PDFUnit.toFixedFloat(maxWidth),
	        sw: this.spaceWidth, //font space width, use to merge adjacent text blocks
        clr: clrId,
        A: "left",
        R: [{
            T: this.flash_encode(text),
            S: this.fontStyleId,
            TS: TS
        }]
    };

    //MQZ.07/29/2013: when color is not in color dictionary, set the original color (oc)
    if (clrId < 0) {
        oneText = _.extend({oc: color}, oneText);
    }

    let rAngle = _textRotationAngle.call(this, matrix2D);
    if (rAngle != 0) {
        nodeUtil.p2jinfo(str + ": rotated " + rAngle + " degree.");
        _.extend(oneText.R[0], {RA: rAngle});
    }

	    targetData.Texts.push(oneText);
}
```
- example usage
```shell
...
    if (!text || text.trim().length < 1)
        return;
    let p = this.getCoords_(x, y);

    let a = processStyle(this.fillStyle || this.strokeStyle);
    let color = (!!a) ? a.color : '#000000';

    this.currentFont.processText(p, text, maxWidth, color, fontSize, this.canvas, this.m_);
};

contextPrototype.strokeText = function(text, x, y, maxWidth) {
    //MQZ. 10/23/2012, yeah, no hollow text for now
    this.fillText(text, x, y, maxWidth);
};
...
```



# <a name="apidoc.module.pdf2json.pdfline"></a>[module pdf2json.pdfline](#apidoc.module.pdf2json.pdfline)

#### <a name="apidoc.element.pdf2json.pdfline.pdfline"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfline (x1, y1, x2, y2, lineWidth, color, dashed)](#apidoc.element.pdf2json.pdfline.pdfline)
- description and source-code
```javascript
pdfline = function (x1, y1, x2, y2, lineWidth, color, dashed) {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };

    this.x1 = x1;
    this.y1 = y1;
    this.x2 = x2;
    this.y2 = y2;
    this.lineWidth = lineWidth || 1.0;
    this.color = color;
    this.dashed = dashed;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.pdfline.prototype"></a>[module pdf2json.pdfline.prototype](#apidoc.module.pdf2json.pdfline.prototype)

#### <a name="apidoc.element.pdf2json.pdfline.prototype.processLine"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfline.prototype.</span>processLine (targetData)](#apidoc.element.pdf2json.pdfline.prototype.processLine)
- description and source-code
```javascript
processLine = function (targetData) {
    let xDelta = Math.abs(this.x2 - this.x1);
    let yDelta = Math.abs(this.y2 - this.y1);
    let minDelta = this.lineWidth;

    let oneLine = {x:0, y:0, w: PDFUnit.toFixedFloat(this.lineWidth), l:0};

    //MQZ Aug.28.2013, adding color support, using color dictionary and default to black
    let clrId = PDFUnit.findColorIndex(this.color);
    if (clrId < 0) {
        oneLine = _.extend({oc: this.color}, oneLine);
    }
    else if (clrId > 0 && clrId < (PDFUnit.colorCount() - 1)) {
        oneLine = _.extend({clr: clrId}, oneLine);
    }

    //MQZ Aug.29 dashed line support
    if (this.dashed) {
        oneLine = _.extend({dsh: 1}, oneLine);
    }

    if ((yDelta < this.lineWidth) && (xDelta > minDelta)) { //HLine
        if (this.lineWidth < 4 && (xDelta / this.lineWidth < 4)) {
            nodeUtil.p2jinfo("Skipped: short thick HLine: lineWidth = " + this.lineWidth + ", xDelta = " + xDelta);
            return; //skip short thick lines, like PA SPP lines behinds checkbox
        }

        oneLine.l = PDFUnit.toFormX(xDelta);
        if (this.x1 > this.x2)
            _setStartPoint.call(this, oneLine, this.x2, this.y2);
        else
            _setStartPoint.call(this, oneLine, this.x1, this.y1);
        targetData.HLines.push(oneLine);
    }
    else if ((xDelta < this.lineWidth) && (yDelta > minDelta)) {//VLine
        if (this.lineWidth < 4 && (yDelta / this.lineWidth < 4)) {
            nodeUtil.p2jinfo("Skipped: short thick VLine: lineWidth = " + this.lineWidth + ", yDelta = " + yDelta);
            return; //skip short think lines, like PA SPP lines behinds checkbox
        }

        oneLine.l = PDFUnit.toFormY(yDelta);
        if (this.y1 > this.y2)
            _setStartPoint.call(this, oneLine, this.x2, this.y2);
        else
            _setStartPoint.call(this, oneLine, this.x1, this.y1);
        targetData.VLines.push(oneLine);
    }
}
```
- example usage
```shell
...
    this.currentFont = null;
}

//private helper methods
let _drawPDFLine = function(p1, p2, lineWidth, color) {
    let dashedLine = _.isArray(this.dashArray) && (this.dashArray.length > 1);
    let pL = new PDFLine(p1.x, p1.y, p2.x, p2.y, lineWidth, color, dashedLine);
    pL.processLine(this.canvas);
};

let _drawPDFFill = function(cp, min, max, color) {
    let width = max.x - min.x;
    let height = max.y - min.y;
    let pF = new PDFFill(cp.x, cp.y, width, height, color);
    pF.processFill(this.canvas);
...
```



# <a name="apidoc.module.pdf2json.pdfunit"></a>[module pdf2json.pdfunit](#apidoc.module.pdf2json.pdfunit)

#### <a name="apidoc.element.pdf2json.pdfunit.pdfunit"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>pdfunit ()](#apidoc.element.pdf2json.pdfunit.pdfunit)
- description and source-code
```javascript
pdfunit = function () {
    // private
    let _id = _nextId++;

    // public (every instance will have their own copy of these methods, needs to be lightweight)
    this.get_id = function() { return _id; };
    this.get_name = function() { return _name + _id; };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit.colorCount"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>colorCount ()](#apidoc.element.pdf2json.pdfunit.colorCount)
- description and source-code
```javascript
colorCount = function () {
    return kColors.length;
}
```
- example usage
```shell
...
let oneLine = {x:0, y:0, w: PDFUnit.toFixedFloat(this.lineWidth), l:0};

//MQZ Aug.28.2013, adding color support, using color dictionary and default to black
let clrId = PDFUnit.findColorIndex(this.color);
if (clrId < 0) {
    oneLine = _.extend({oc: this.color}, oneLine);
}
else if (clrId > 0 && clrId < (PDFUnit.colorCount() - 1)) {
    oneLine = _.extend({clr: clrId}, oneLine);
}

//MQZ Aug.29 dashed line support
if (this.dashed) {
    oneLine = _.extend({dsh: 1}, oneLine);
}
...
```

#### <a name="apidoc.element.pdf2json.pdfunit.findColorIndex"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>findColorIndex (color)](#apidoc.element.pdf2json.pdfunit.findColorIndex)
- description and source-code
```javascript
findColorIndex = function (color) {
    if (color.length === 4)
        color += "000";
    //MQZ. 07/29/2013: if color is not in dictionary, just return -1. The caller (pdffont, pdffill) will set the actual color
    return kColors.indexOf(color);
}
```
- example usage
```shell
...
this.width = width;
this.height = height;
this.color = color;
    };

    // public (every instance will share the same method, but has no access to private fields defined in constructor)
    cls.prototype.processFill = function (targetData) {
let clrId = PDFUnit.findColorIndex(this.color);

let oneFill = {x:PDFUnit.toFormX(this.x),
               y:PDFUnit.toFormY(this.y),
               w:PDFUnit.toFormX(this.width),
               h:PDFUnit.toFormY(this.height),
               clr: clrId};
...
```

#### <a name="apidoc.element.pdf2json.pdfunit.getColorByIndex"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>getColorByIndex (clrId)](#apidoc.element.pdf2json.pdfunit.getColorByIndex)
- description and source-code
```javascript
getColorByIndex = function (clrId) {
    return kColors[clrId];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit.pointToPixel"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>pointToPixel (point)](#apidoc.element.pdf2json.pdfunit.pointToPixel)
- description and source-code
```javascript
pointToPixel = function (point) {// Point unit (1/72 an inch) to pixel units
    return point * _pixelPerPoint;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit.toFixedFloat"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFixedFloat (fNum)](#apidoc.element.pdf2json.pdfunit.toFixedFloat)
- description and source-code
```javascript
toFixedFloat = function (fNum) {
    return parseFloat(fNum.toFixed(3));
}
```
- example usage
```shell
...
        // adding TS to better describe text style [fontFaceId, fontSize, 1/0 for bold, 1/0 for italic];
        let TS = [this.faceIdx, this.fontSize, this.bold?1:0, this.italic?1:0];

        let clrId = PDFUnit.findColorIndex(color);

        let oneText = {x: PDFUnit.toFormX(p.x) - 0.25,
y: PDFUnit.toFormY(p.y) - 0.75,
w: PDFUnit.toFixedFloat(maxWidth),
	        sw: this.spaceWidth, //font space width, use to merge adjacent text blocks
clr: clrId,
A: "left",
R: [{
    T: this.flash_encode(text),
    S: this.fontStyleId,
    TS: TS
...
```

#### <a name="apidoc.element.pdf2json.pdfunit.toFormPoint"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormPoint (viewportX, viewportY)](#apidoc.element.pdf2json.pdfunit.toFormPoint)
- description and source-code
```javascript
toFormPoint = function (viewportX, viewportY) {
    return [(viewportX / _pixelXPerGrid), (viewportY / _pixelYPerGrid)];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit.toFormX"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormX (viewportX)](#apidoc.element.pdf2json.pdfunit.toFormX)
- description and source-code
```javascript
toFormX = function (viewportX) {
    return cls.toFixedFloat(viewportX / _pixelXPerGrid);
}
```
- example usage
```shell
...
this.Fields = [];
//form elements: radio buttons and check boxes
this.Boxsets = [];

//public properties
Object.defineProperty(this, 'width', {
    get:function () {
        return PDFUnit.toFormX(this.viewport.width);
    },
    enumerable:true
});

Object.defineProperty(this, 'height', {
    get:function () {
        return PDFUnit.toFormY(this.viewport.height);
...
```

#### <a name="apidoc.element.pdf2json.pdfunit.toFormY"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toFormY (viewportY)](#apidoc.element.pdf2json.pdfunit.toFormY)
- description and source-code
```javascript
toFormY = function (viewportY) {
    return cls.toFixedFloat(viewportY / _pixelYPerGrid);
}
```
- example usage
```shell
...
                return PDFUnit.toFormX(this.viewport.width);
            },
            enumerable:true
        });

        Object.defineProperty(this, 'height', {
            get:function () {
                return PDFUnit.toFormY(this.viewport.height);
            },
            enumerable:true
        });
    };
    // inherit from event emitter
	nodeUtil.inherits(cls, nodeEvents.EventEmitter);
...
```

#### <a name="apidoc.element.pdf2json.pdfunit.toPixelX"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toPixelX (formX)](#apidoc.element.pdf2json.pdfunit.toPixelX)
- description and source-code
```javascript
toPixelX = function (formX) {
    return Math.round(formX * _pixelXPerGrid);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pdf2json.pdfunit.toPixelY"></a>[function <span class="apidocSignatureSpan">pdf2json.pdfunit.</span>toPixelY (formY)](#apidoc.element.pdf2json.pdfunit.toPixelY)
- description and source-code
```javascript
toPixelY = function (formY) {
    return Math.round(formY * _pixelYPerGrid);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.ptixmlinject"></a>[module pdf2json.ptixmlinject](#apidoc.module.pdf2json.ptixmlinject)

#### <a name="apidoc.element.pdf2json.ptixmlinject.ptixmlinject"></a>[function <span class="apidocSignatureSpan">pdf2json.</span>ptixmlinject ()](#apidoc.element.pdf2json.ptixmlinject.ptixmlinject)
- description and source-code
```javascript
ptixmlinject = function () {
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pdf2json.ptixmlinject.prototype"></a>[module pdf2json.ptixmlinject.prototype](#apidoc.module.pdf2json.ptixmlinject.prototype)

#### <a name="apidoc.element.pdf2json.ptixmlinject.prototype.getFields"></a>[function <span class="apidocSignatureSpan">pdf2json.ptixmlinject.prototype.</span>getFields (pageNum)](#apidoc.element.pdf2json.ptixmlinject.prototype.getFields)
- description and source-code
```javascript
getFields = function (pageNum) {
		return ptiPageArray[pageNum];
	}
```
- example usage
```shell
...
let errMsg = 'An error occurred while rendering the page ' + (this.id + 1) +
    ':\n' + error.message +
    ':\n' + error.stack;
errorCallBack(errMsg);
            }
            else {
if (this.ptiParser) {
    let extraFields = this.ptiParser.getFields(parseInt(this.id) + 1);
    _.each(extraFields, _.bind(_addField, this));
}

_.extend(this, ctx.canvas);
this.stats = this.pdfPage.stats;

nodeUtil.p2jinfo('page ' + (this.id + 1) + ' is rendered successfully.');
...
```

#### <a name="apidoc.element.pdf2json.ptixmlinject.prototype.parseXml"></a>[function <span class="apidocSignatureSpan">pdf2json.ptixmlinject.prototype.</span>parseXml (filePath, callback)](#apidoc.element.pdf2json.ptixmlinject.prototype.parseXml)
- description and source-code
```javascript
parseXml = function (filePath, callback) {

		fs.readFile(filePath, 'utf8', function (err,data) {
			if (err) {
                callback(err);
			}
			else {
				xmlData = data;

				var parser = new DOMParser();
				var dom = parser.parseFromString(xmlData);
				var root = dom.documentElement;

				var xmlFields = root.getElementsByTagName("field");
				var fields = [];

				for(var i=0;i<xmlFields.length;i++){
					var id = xmlFields[i].getAttribute('id');
					var xPos = xmlFields[i].getAttribute('x');
					var yPos = xmlFields[i].getAttribute('y');
					var width = xmlFields[i].getAttribute('width');
					var height = xmlFields[i].getAttribute('height');
					var type = xmlFields[i].getAttribute('xsi:type');
					var page = xmlFields[i].getAttribute('page');
					var fontName = xmlFields[i].getAttribute('fontName');
					var fontSize = xmlFields[i].getAttribute('fontSize');

					var item = {};
					
					var rectLeft = parseInt(xPos) - 21; //was 23.5
					var rectTop = parseInt(yPos) - 20;//was 23
					var rectRight = parseInt(rectLeft) + parseInt(width) - 4;
					var rectBottom = parseInt(rectTop) + parseInt(height) - 4;
					
					item.fieldType="Tx";
					if (type == "Boolean") {
						item.fieldType="Btn";
					}
					else  if (type=="SSN" ||  type=="Phone" || type=="zip") {
						item.TName = type.toLowerCase();
					}
					item.alternativeText = "";
					item.fullName = id;
					item.fontSize = fontSize;
					item.subtype = "Widget";

					item.rect = [rectLeft, rectTop, rectRight, rectBottom];;

					fields.push(item);
					
					ptiPageArray[parseInt(page)]=fields;
				}
				
			}
			callback();
		});
	}
```
- example usage
```shell
...
if ((fieldInfoXMLPath.indexOf(_sufInfo) < 1) || (!fs.existsSync(fieldInfoXMLPath))) {
    return;
}
nodeUtil.p2jinfo("About to load fieldInfo XML : " + fieldInfoXMLPath);

let PTIXmlParser = require('./ptixmlinject');
this.ptiParser = new PTIXmlParser();
this.ptiParser.parseXml(fieldInfoXMLPath, err => {
    if (err) {
        nodeUtil.p2jwarn("fieldInfo XML Error: " + JSON.stringify(err));
        this.ptiParser = null;
    }
    else {
        nodeUtil.p2jinfo("fieldInfo XML loaded.");
    }
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
