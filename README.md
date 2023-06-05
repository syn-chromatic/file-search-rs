# File Search Rust

## `➢` Information
A Rust utility to search files with various filters such as:
* Exclusive Filenames
* Exclusive Extensions
* Exclude Directories

The algorithm recursively searches through all of the directories from the specified root.

## `➢` Example Usage
```rust
let mut file_search: FileSearch = FileSearch::new();

// Set the root directory for the file search
let root: &str = "./";
file_search.set_root(root);

// Below examples are optional

// Specify filenames to exclusively search for
let exclusive_filenames: Vec<&str> = vec!["README"];
file_search.set_exclusive_filenames(exclusive_filenames);

// Specify extensions to exclusively search for
let exclusive_exts: Vec<&str> = vec![".md"];
file_search.set_exclusive_extensions(exclusive_exts);

// Specify directories to exclude from the search
// This excludes the path and not the directory name
let exclude_dirs: Vec<&str> = vec!["./excluded_dir"];
file_search.set_exclude_directories(exclude_dirs);

// Perform the file search and get the result
let files: Vec<PathBuf> = file_search.search_files();
```
