## 本文实例代码采用poi版本3.11

## 创建图纸
```java
HSSFPatriarch patriarch = (HSSFPatriarch) sheet.createDrawingPatriarch();
```

## 通过锚定位图片位置及大小
```java
anchor = new HSSFClientAnchor();
anchor.setAnchorType(2);
// 计算单元格的长宽
double cellWidth = sheet.getColumnWidthInPixels(cell.getColumnIndex());
double cellHeight = cell.getRow().getHeightInPoints() / 72 * 96;
// 计算需要的长宽比例的系数
double a = standardWidth / cellWidth;
double b = standardHeight / cellHeight;
anchor.setCol1(j);
anchor.setRow1(i);
HSSFPicture picture = patriarch.createPicture(anchor, wb.addPicture(byteArrayOut.toByteArray(), HSSFWorkbook.PICTURE_TYPE_JPEG));
picture.resize(a, b);
```




