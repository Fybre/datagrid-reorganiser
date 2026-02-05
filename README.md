# Therefore Datagrid Reorganiser

A web-based tool for reordering datagrid columns in Therefore XML configuration files.

## 🎯 Problem

The Therefore eForm designer doesn't allow you to change the order of datagrid columns. To reorder them, you have to manually edit the XML export file - finding the datagrid and rearranging the components array.

## ✅ Solution

This tool provides a visual drag-and-drop interface to reorder datagrid columns, then exports the modified XML with only the component order changed.

## 🚀 Usage

1. **Open** `index.html` in any modern web browser
2. **Drag and drop** your Therefore XML file onto the drop zone (or click to browse)
3. The tool will **automatically find** all eForms and their datagrids
4. **Drag column headers** to reorder them as needed
5. Click **"Save Modified XML"** to download the updated file

## 📁 File Structure

```
datagrid-reorganiser/
├── index.html          # Main application (single file)
├── README.md           # This file
└── samples/
    └── test.xml        # Sample Therefore XML for testing
```

## 🧪 Testing

A sample XML file (`samples/test.xml`) is included for testing. It contains:
- **EForm**: "Settlement for Travel"
- **Datagrid**: "Results" with 9 columns (Reference, Applicant, Amount, Detail, View, Select, DocId, Application Date, jsonData)

## 🔧 How It Works

1. **Parses** the XML to find `<EForm>` elements
2. **Extracts** the JSON configuration from `<FDef>` tags
3. **Locates** all objects with `"type": "datagrid"`
4. **Renders** a visual mockup of each datagrid's columns
5. **Tracks** drag-and-drop reordering with SortableJS
6. **Re-serializes** the XML with the new component order

## 📝 Notes

- The tool preserves **all** XML content exactly as-is
- Only the order of components within datagrids is modified
- No data is sent to any server - everything runs locally in your browser

## 📄 License

MIT
