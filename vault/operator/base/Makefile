MANIFESTS = bank-vault-operator.yaml

all: $(MANIFESTS)

bank-vault-operator.yaml: $(wildcard src/*)
	kustomize build --enable-helm src/ > $@ || { rm -f $@; exit 1; }

clean:
	rm -f $(MANIFESTS)
