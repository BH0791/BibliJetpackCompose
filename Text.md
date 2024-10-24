Text
----

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
@Composable
fun Text(
    text: AnnotatedString,
    modifier: Modifier = Modifier,
    color: Color = Color.Unspecified,
    fontSize: TextUnit = TextUnit.Unspecified,
    fontStyle: FontStyle? = null,
    fontWeight: FontWeight? = null,
    fontFamily: FontFamily? = null,
    letterSpacing: TextUnit = TextUnit.Unspecified,
    textDecoration: TextDecoration? = null,
    textAlign: TextAlign? = null,
    lineHeight: TextUnit = TextUnit.Unspecified,
    overflow: TextOverflow = TextOverflow.Clip,
    softWrap: Boolean = true,
    maxLines: Int = Int.MAX_VALUE,
    minLines: Int = 1,
    inlineContent: Map<String, InlineTextContent> = mapOf(),
    onTextLayout: (TextLayoutResult) -> Unit = {},
    style: TextStyle = LocalTextStyle.current
): Unit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
### Parameters
| Syntax                                                  | Description                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| text: AnnotatedString                                   | le texte à afficher                                                                                                                                                                                                                                                                                                                 |
| modifier: Modifier = Modifier                           | the Modifier to be applied to this layout node                                                                                                                                                                                                                                                                                      |
| color: Color = Color.Unspecified                        | Color to apply to the text. If Color.Unspecified, and style has no color set, this will be LocalContentColor.                                                                                                                                                                                                                       |
| fontSize: TextUnit = TextUnit.Unspecified               | the size of glyphs to use when painting the text. See TextStyle.fontSize.                                                                                                                                                                                                                                                           |
| fontStyle: FontStyle? = null                            | the typeface variant to use when drawing the letters (e.g., italic). See TextStyle.fontStyle.                                                                                                                                                                                                                                       |
| fontWeight: FontWeight? = null                          | the typeface thickness to use when painting the text (e.g., FontWeight.Bold).                                                                                                                                                                                                                                                       |
| fontFamily: FontFamily? = null                          | the font family to be used when rendering the text. See TextStyle.fontFamily.                                                                                                                                                                                                                                                       |
| letterSpacing: TextUnit = TextUnit.Unspecified          | the amount of space to add between each letter. See TextStyle.letterSpacing.                                                                                                                                                                                                                                                        |
| textDecoration: TextDecoration? = null                  | the decorations to paint on the text (e.g., an underline). See TextStyle.textDecoration.                                                                                                                                                                                                                                            |
| textAlign: TextAlign? = null                            | the alignment of the text within the lines of the paragraph. See TextStyle.textAlign.                                                                                                                                                                                                                                               |
| lineHeight: TextUnit = TextUnit.Unspecified             | line height for the Paragraph in TextUnit unit, e.g. SP or EM. See TextStyle.lineHeight.                                                                                                                                                                                                                                            |
| overflow: TextOverflow = TextOverflow.Clip              | how visual overflow should be handled.                                                                                                                                                                                                                                                                                              |
| softWrap: Boolean = true                                | whether the text should break at soft line breaks. If false, the glyphs in the text will be positioned as if there was unlimited horizontal space. If softWrap is false, overflow and TextAlign may have unexpected effects.                                                                                                        |
| maxLines: Int = Int.MAX_VALUE                           | An optional maximum number of lines for the text to span, wrapping if necessary. If the text exceeds the given number of lines, it will be truncated according to overflow and softWrap. It is required that 1 <= minLines<= maxLines.                                                                                              |
| minLines: Int = 1                                       | The minimum height in terms of minimum number of visible lines. It is required that 1 <= minLines<= maxLines.                                                                                                                                                                                                                       |
| inlineContent: Map<String, InlineTextContent> = mapOf() | a map storing composables that replaces certain ranges of the text, used to insert composables into text layout. See InlineTextContent.                                                                                                                                                                                             |
| onTextLayout: (TextLayoutResult) -> Unit = {}           | callback that is executed when a new text layout is calculated. A TextLayoutResult object that callback provides contains paragraph information, size of the text, baselines and other details. The callback can be used to add additional decoration or functionality to the text. For example, to draw selection around the text. |
| style: TextStyle = LocalTextStyle.current               | style configuration for the text such as color, font, line height etc.                                                                                                                                                                                                                                                              |