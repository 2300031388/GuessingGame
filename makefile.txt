# Define variables for file names
README = README.md
SCRIPT = guessinggame.sh

# Default target
all: $(README)

# Rule to create README.md
$(README): $(SCRIPT)
	echo "# Guessing Game Project" > $(README)
	echo "Generated on: $$(date)" >> $(README)
	echo "Number of lines in guessinggame.sh: $$(wc -l < $(SCRIPT))" >> $(README)

# Clean target to remove generated files
clean:
	rm -f $(README)
