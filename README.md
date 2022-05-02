# structlan
Just another code generator for binary data format parser\serializers

Interesting features include:
+ It's very simple XD
  + An implementation (a code generator tool) is just a few files of source code (at least in Java, maybe not in assembly XD )
  + There's no special nonstandard input file format (see other main bullet)
  + It works solely in terms of bytes (at least for now).  Splitting bitfields is left to the user to do manually (or not do, if they prefer; USB code and docs often conflate split and unsplit bmRequestType, for example).
+ The input file format is almost JSON!  (it's JSON but with multiline string literals because..dear holy god, copying documentation in and dealing with double-quote escape syntax is bad enough, imagine converting entire paragraphs to use "\n"s on one line!!  ~~kill me now~~ XD )
 + (although the code uses an abstract syntax tree based on java.lang.String and java.util.List and etc. (which I call GDS — Generic DataStructures) from a JSON decoder that decodes to GDS, so it would be quite easy to have it use ~~CBOR~~ YAML XD )
+ This implementation is written in Java but it's intended to be output-language-agnostic.


(TODO upload it XD'')

(TODO upload InfileGen, which this "reference implementation" is actually a plugin for XD'')
