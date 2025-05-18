MANIFESTS = dex.yaml

all: $(MANIFESTS)

dex.yaml: $(wildcard src/*)
	kustomize build --enable-helm src | sed '/: null$$/ d' > $@ || { rm -f $@; exit 1; }

clean:
	rm -f $(MANIFESTS)
