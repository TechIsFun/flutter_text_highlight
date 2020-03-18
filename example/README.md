## Example

You can see the complete example in the [GitHub Repository](https://github.com/desconexo/flutter_text_highlight/tree/master/example).

Import the highlight library
``` dart
import 'package:flutter_text_highlight/flutter_text_highlight.dart';
```

You should use the `HighlightedWord` class to specify the dictionary words in a Map object
``` dart
Map<String, HighlightedWord> words = {
    "Flutter": HighlightedWord(
        onTap: () {
            print("Flutter");
        },
        textStyle: textStyle,
    ),
    "open-source": HighlightedWord(
        onTap: () {
            print("open-source");
        },
        textStyle: textStyle,
    ),
    "Android": HighlightedWord(
        onTap: () {
            print("Android");
        },
        textStyle: textStyle,
    ),
};
```

Now you can call the `TextHighlight` widget
``` dart
TextHighlight(
    text: text, // You need to pass the string you want the highlights
    words: words, // Your dictionary words
    textStyle: TextStyle( // You can set the general style, like a Text()
        fontSize: 20.0,
        color: Colors.black,
    ),
    textAlign: TextAlign.justify, // You can use any attribute of the RichText widget
),
```