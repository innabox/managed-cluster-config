all: manifests.yaml

# Generate manifests from the helm chart using `kustomize build --enable-helm`.
manifests.yaml: $(wildcard src/*)
	kustomize build --enable-helm src > $@ || { rm -f $@; exit 1; }

clean:
	rm -f manifests.yaml
