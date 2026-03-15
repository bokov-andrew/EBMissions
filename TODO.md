# Todo List for Easter Egg Hunt Graph Generator

Based on the specs and current progress in main.R, here's a todo list for completing the Easter egg hunt graph generator:

1. **Implement graph construction logic**: Create a function to randomly connect nodes (hiding spots) into a directed graph, respecting max incoming/outgoing edges, min incoming edges (1 unless 0), and eligible targets based on subclusters. Use the processed data (dat2) as input.

2. **Handle edge constraints and randomization**: Ensure connections are acyclic or handle cycles if needed; implement retry logic for failed connections due to constraints; validate the final graph meets all rules.

3. **Generate Graphviz DOT file**: Write a function to output the graph as a DOT file, including nodes (hiding spots and clues) and directed edges.

4. **Generate SVG visualization**: Use a library (e.g., DiagrammeR or system call to Graphviz) to convert the DOT file to SVG.

5. **Create output data frame**: Build a data frame with one column for hiding spots and another for concatenated clues leading out from each spot (based on outgoing edges).

6. **Export spreadsheet**: Use rio::export to save the data frame as a spreadsheet (e.g., CSV or XLSX).

7. **Add main execution flow**: Integrate all steps into a cohesive script that reads input, processes data, builds graph, generates outputs, and handles errors.

8. **Test with example data**: Run the full script on the provided example to verify outputs and constraints. (done — script now builds a graph without constraint warnings.)

9. **Persist output artifacts**: Add functionality to write the graph as a DOT file, render an SVG, and export the clue graph as a spreadsheet.

10. **Add command-line or configurable input**: Allow `data_path` to be set via arguments or environment for real input files.

11. **Code review and cleanup**: Ensure adherence to coding style (e.g., mandatory semicolons, line breaks, comments); remove unused code; optimize for readability.
