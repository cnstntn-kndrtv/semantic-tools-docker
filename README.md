# Semantic-tools-docker
Some tools to work with ontologies: rdf2hdt, hdt2rdf, raptor (rapper), xsltproc...

## Available utils:  
[HDT Tools:](https://github.com/rdfhdt/hdt-cpp "HDT Tools")  

    - rdf2hdt  
    - hdt2rdf  
    - hdtSearch  

[Raptor (rapper)](http://librdf.org/raptor/rapper.html "rapper"). C library that provides a set of parsers and serializers that generate Resource Description Framework (RDF) triples by parsing syntaxes or serialize the triples into a syntax. The supported parsing syntaxes are RDF/XML, N-Quads, N-Triples 1.0 and 1.1, TRiG, Turtle 2008 and 2013, RDFa 1.0 and 1.1, RSS tag soup including all versions of RSS, Atom 1.0 and 0.3, GRDDL and microformats for HTML, XHTML and XML. The serializing syntaxes are RDF/XML (regular, abbreviated, XMP), Turtle 2013, N-Quads, N-Triples 1.1, Atom 1.0, RSS 1.0, GraphViz DOT, HTML, JSON and mKR.
    
[Xsltproc](http://xmlsoft.org/XSLT/xsltproc.html 'xsltproc') command line xslt processor  

[Libz](http://www.zlib.net "libz"). A compression library provides in-memory compression and decompression functions, including integrity checks of the uncompressed data. This version of the library supports only one compression method (deflation) but other algorithms will be added later and will have the same stream interface.  

[Serd](http://drobilla.net/software/serd "Serd") a lightweight C library for RDF syntax which supports reading and writing Turtle and NTriples.  

[Kyoto Cabinet](http://fallabs.com/kyotocabinet/) (optional) Enables generating big RDF datasets on machines without much RAM memory, by creating a temporary Kyoto Cabinet database. The dependency is deactivated by default; to activate it, uncomment the line `KYOTO_SUPPORT=true` in the `Makefile` and edit the library include path (`INCLUDES=`) as needed.  

## Usage example

Pull Docker image  

    docker pull cnstntnkndrtv/semantic-tools-docker  

Help  

    docker run -it --rm cnstntnkndrtv/semantic-tools-docker rdf2hdt -h

Example  

    $ docker run -it --rm -v "$(pwd)":/data cnstntnkndrtv/semantic-tools-docker rdf2hdt -f turtle /data/myfile.turtle /data/myfile.hdt

