# Semantic-tools-docker
Some tools to work with ontologies: rdf2hdt, hdt2rdf, raptor (rapper), xsltproc...

## Available utils:  
- rdf2hdt
- hdt2rdf
- hdtSearch

- Raptor (rapper)
- Xsltproc

- Kyoto Cabinet
- Libz
- Serd

## Usage  
### RDF to HDT  

Help  

    docker run -it --rm rfdhdt/hdt-cpp rdf2hdt -h

Example  

    $ docker run -it --rm -v "$(pwd)":/data rfdhdt/hdt-cpp rdf2hdt -f turtle /data/myfile.turtle /data/myfile.hdt

$ docker run -it --rm -v "$(pwd)":/data rfdhdt/hdt-cpp hdtSearch /data/myfile.hdt

### HDT to RDF  

Help  

    docker run -it --rm rfdhdt/hdt-cpp hdt2rdf -h

Example  

    $ docker run -it --rm -v "$(pwd)":/data rfdhdt/hdt-cpp hdt2rdf -f turtle /data/myfile.hdt /data/myfile.turtle

# HDT search

Help
    $ docker run -it --rm -v "$(pwd)":/data rfdhdt/hdt-cpp hdtSearch -h

Example  

    $ docker run -it --rm -v "$(pwd)":/data rfdhdt/hdt-cpp hdtSearch /data/myfile.hdt