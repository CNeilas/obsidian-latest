Example of a table:

```
<table>
	<tr>
		<th>First Header</th>
		<th>Second Header</th>
	</tr>
	<tr>
		<td>This is a data cell</td>
		<td>This is also a data cell!</td>
	</tr>
</table>
```

![[Table_img.png]]

You can add table headers with:

```
<tr>
	<th>Header</th>
</tr>
```

and just usual table data with:

```
<tr>
	<td>This is a data cell</td>
</tr>
```

## Table caption

You can add a caption with a title about what the table shows.

```
<table>
	<caption>...</caption>
	<tr>
	...
	</tr>
</table>
```

## Thead, tbody and tfoot

```
<thead></thead> // is usually the first line
```

```
<tbody></tbody> // wraps the main part of the table
```

```
// this wraps either final row with items in the previous row summed or smt idk, last line
<tfoot></tfoot>
```

You can also add styles to these but this is self explanatory.

## Scope attribute

This is used to to tell screen readers what exactly is the header for, it's column or row.

```
<thead>
	<tr>
		<th scope="col">Purchase</th>
		<th scope="col">Location</th>
		<th scope="col">Date</th>
	</tr>
</thead>

<tr>
	<th scope="row">Haircut</th>
	<td>Hairdresser</td>
	<td>12/09</td>
</tr>
```

```
<tr>
		// I assume this makes it take up two cells in a row
	 <th rowspan="2" scope="rowgroup">The Netherlands</th>
	 <th scope="row">Amsterdam</th>
	 <td>89</td>
	 <td>34</td>
	 <td>69</td>
</tr>
```

```
<thead>
	// I assume this takes up three cells in a column
	<tr>
		<th colspan="3" scope="colgroup">Clothes</th>
	</tr>
	<tr>
		<th scope="col">Trousers</th>
		<th scope="col">Skirts</th>
		<th scope="col">Dresses</th>
	</tr>
</thead>
```

## Id's and headers

You basically give table headers id's and then use a `headers` attribute on table data and put the id's in the headers attribute.

https://css-tricks.com/complete-guide-table-element/ reference this when making tables.