#
# Простейший Makefile для создания отчёта
#

PDF=report.pdf

# Используемые программы
PDFLATEX = xelatex -interaction=nonstopmode -shell-escape

LAB=../net

TEX=tex
TEXPREAMBLE=../../doc

.PHONY: clean
all : $(PDF)
report : $(PDF)

# Основная цель сборки --- отчет
$(PDF) : $(TEX)/report.tex $(TEXPREAMBLE)/preamble.tex
	cd $(TEX) && $(PDFLATEX) report.tex && $(PDFLATEX) report.tex && cp $(PDF) ..

# Удаление ВСЕХ временных файлов
clean:
	find $(TEX)/ -regextype posix-egrep -type f ! -regex ".*\.(sty|tex|clo|cls|bib|bst|gitignore)" -exec $(RM) {} \; ;

