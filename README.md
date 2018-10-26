### TerminalTable
---
https://github.com/tj/terminal-table

```
gem install terminal-table

```


```ruby
require 'terminal-table'
rows = []
rows << ['One', 1]
rows << ['Two', 2]
rows << ['Three', 3]
table = Terminal::Table.new :rows => rows

table = Terminal::Table.new do |t|
  r.rows = rows
end
table = Terminal::Table.new do
  self.rows = rows
end

table = Terminal::Table.new do |t|
  t << ['One', 1]
  t.add_row ['Two', 2]
end

table = Terminal::Table.new do |t|
  t << ['One', 1]
  t << :separator
  t.add_row ['Two', 2]
  t.add_separator
  t.add_row ['Three', 3]
end
#> puts table

table = Terminal::Table.new do |t|
  t << ['One', 1]
  t << :separator
  t.add_row ["Two\nDouble", 2]
  t.add_separator
  t.add_row ['Three', 3]
end
#> puts table

table = Terminal::Table.new :headings => ['Word', 'Number'], :rows => rows

table = Terminal::Table.new :title => "Cheatsheet", :headings => ["Word", 'Number'], :rows => rows

table.align_column(1, :right)

table << ["Four", {:value => 4.0, :alignment => :center}]
#> puts table

table = Terminal::Table.new :headings => ['Word', 'Number'], :rows => rows, :style => {:width => 80}
#> puts table

table.style = {:width => 40, :padding_left => 3, :border_x => "=", :border_i => "x"}

table = Terminal::Table.new do |t|
  t.add_row [1, 'One']
  t.add_row [2, 'Two']
  t.add_row [3, 'Three']
  t.style = {:all_separators => true}
end
#> puts table

table = Terminal::Table.new do |t|
  t.headings = ['id', 'name']
  t.rows = [[1, 'One'], [2, 'Two'], [3, 'Three']]
  t.style = { :border_top => false, :border_bottom => false}
end

Terminal::Table::Style.defaults = {:width => 80}

table = Terminal::Table.new
table.title = "Cheatsheet"
table.headings = ['Word', 'Number']
table.rows = rows
table.style = {:width => 40}







```

```
```
