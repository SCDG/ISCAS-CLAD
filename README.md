# ISCAS-CLAD

ISCAS-CLAD is a large dataset of Chinese Document Layout Analysis images, of which the layout is annotated with both bounding boxes and polygonal segmentations.

## Introduce
ISCAS-CLAD is a DLA Dataset for Chinese literature class (thesis) scenario. It contains the following 8 labels:
|Text|Title|Figure|Table|Header|Footer|Reference|Equation|

ISCAS_CLAD contains a total of 3000 images in the training set and 600 images in the validation set, located in the "train" and "val" directories. Each sample corresponds to a txt file and an xml file.

## Headlines
`19/April/2023` - released ISCAS-CLAD

## Getting data
Currently, we provide some sample data and annotated text to demonstrate. We will gradually update more in the future.

## Annotation format
我们的标注工具在LabelImg的基础上添加了预标注功能，首先用预训练模型来对文档图像预标注，然后对预标注标签进行人工矫正，标注格式包含Yolo格式和VOC格式；
下面分别说一下数据格式：
------------YOLO-------------
label_index center_x center_y w h

17 0.157718 0.787129 0.090604 0.017327
15 0.501678 0.866955 0.781879 0.097772
15 0.707215 0.448020 0.387584 0.059406

------------VOC--------------

<annotation>
	<folder>image</folder>
	<filename>1.png</filename>
	<path>D:\iscas\1.layout_analysis\dataset\ChineseLayoutAnalysys\image\1.png</path>
	<source>
		<database>Unknown</database>
	</source>
	<size>
		<width>596</width>
		<height>808</height>
		<depth>3</depth>
	</size>
	<segmented>0</segmented>
	<object>
		<name>Title</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>67</xmin>
			<ymin>629</ymin>
			<xmax>121</xmax>
			<ymax>643</ymax>
		</bndbox>
	</object>
</annotation>

##Convert YOLO format to COCO format.

```
# train
python3 

# val
python3 
```

## Cite us

Todo

## Examples


