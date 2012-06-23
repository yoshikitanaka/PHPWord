PHPWord
=======
## colspan

    $table = $section->addTable();

    $table->addRow();
    $styleCell=array('gridSpan' => 2);
    $table->addCell(100, $styleCell)->addText('Colspan');
    $table->addCell(100)->addText('Colspan2');
    $table->addRow();
    $table->addCell(100)->addText('Colspan3');
    $table->addCell(100)->addText('Colspan4');
    $table->addCell(100)->addText('Colspan5');
    $section->addTextBreak(10);
    
    
## rowspan

    
    $table = $section->addTable();
    
    $table->addRow();
    //first cell expected to be rowspanned
    $table->addCell(100,array('vMerge' => 'restart'))->addText('1');
    //ordinary cell
    $table->addCell(100)->addText('2');
    $table->addRow();
    //merge cell to cell above(first cell)
    //this technique make empty cell which merged with above cell that //hold 'restart' style
    $table->addCell(100,array('vMerge' => 'fusion'));
    //ordinary cell
    $table->addCell(100)->addText('3');
