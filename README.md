# python_34
python_34


# Simple Tree Graph Example

import networkx as nx  # For creating graph structures
import matplotlib.pyplot as plt  # For drawing graphs

# Create a new graph
tree = nx.DiGraph()  # Directed graph (for tree)

# Add edges (parent -> child)
tree.add_edges_from([
    ("Root", "Child1"),
    ("Root", "Child2"),
    ("Child1", "Grandchild1"),
    ("Child1", "Grandchild2"),
    ("Child2", "Grandchild3")
])

# Draw the tree
pos = nx.spring_layout(tree)  # Layout for nodes
nx.draw(tree, pos, with_labels=True, node_color="lightblue", node_size=2000, arrows=True)
plt.title("Simple Tree Graph")
plt.show()
