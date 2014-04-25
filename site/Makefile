bootstrap := "http://netdna.bootstrapcdn.com/bootstrap/3.1.1/css/bootstrap.min.css"

files := index.html tutorial.html
deps = bootstrap-custom.css background.jpg
install := $(files) $(deps)

all: $(files)

install: $(files)
	cp -a $(install) ../

%.html: %.md template.html $(deps)
	pandoc $< -o $@ --smart --template template.html \
	  --css $(bootstrap) \
	  --css bootstrap-custom.css \
	  --toc --toc-depth 2

clean:
	-rm -f $(files)
