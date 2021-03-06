# 胶囊内镜数据集整理操作步骤

## I. 胶囊内镜老数据集
### 1. 数据集的重组
#### 1.1. 先确定老数据集来自哪些病例。
#### 1.2. 拿到对应的病例报告。
#### 1.3. 根据其中的病例号、视频数量等信息，按照《标注文件目录结构和文件命名规范》中胶囊内镜部分的内容来设置目录结构。
#### 1.4. 使用“胶囊内镜影像软件”将视频原数据格式转换成 .avi格式，按照《标注文件目录结构和文件命名规范》中胶囊内镜部分的内容来命名并放在对应的目录中。
#### 1.5. 使用VLC Media Player抽取视频中所有帧的图片，按照《标注文件目录结构和文件命名规范》中胶囊内镜部分的内容导出到对应目录中。操作步骤见第III部分。
#### 1.6. 完成收集老数据集的全部视频和所有帧的图片后，传给王玺喆。
#### 1.7. 王玺喆完成该数据集的新、旧版本之间所有图和标注的对应匹配，把分类数据集传给曹骧并重新上传到标注网站。
#### 1.8. 标注网站需要支持读取数据集的目录结构。

## II. 胶囊内镜新数据集
### 1. 数据集的整理
#### 1.1. 先确定新数据集包含哪些病例，之后的工作同第I部分的1.1. ～ 1.5.。
#### 1.2. 完成全部视频和所有帧的图片的收集后，开始图片分类工作。
#### 1.3. 根据病例和视频信息，并按照《标注文件目录结构和文件命名规范》中胶囊内镜部分的内容来设置disease目录和其下的各级目录。
#### 1.4. 根据病例和视频信息，从其frames目录中复制病变图片到对应目录中，不要改变图片原有的文件名，以保证图片可追溯。
#### 1.6. 分类完成数据集后，上传到标注网站。

## III. VLC Media Player的使用
### 1. 下载并安装
### 2. 设置VLC Media Player，使得VLC Media Player可以保存视频的每一帧
#### 2.1. 打开VLC Media Player，点击“工具”，“偏好设置”
<img src="https://github.com/wangxizhe2017/XY_Cap_Endo_Dataset_Guide/blob/main/images/1.png" width="400">

#### 2.2. 点击左下角“显示设置”中的“全部”
<img src="https://github.com/wangxizhe2017/XY_Cap_Endo_Dataset_Guide/blob/main/images/2.png" width="450">

#### 2.3. 在左侧list中点击“视频”，“滤镜”
#### 2.4. 在右侧“滤镜”中，勾选“场景视频滤镜”，保存。
<img src="https://github.com/wangxizhe2017/XY_Cap_Endo_Dataset_Guide/blob/main/images/3.png" width="450">

#### 2.5. 关闭VLC Media Player，再打开，设置才会生效。
#### 2.6. 再次点击“工具”，“偏好设置”，左下角“显示设置”中的“全部”，左侧list中的“视频”，展开“滤镜”，点击“场景滤镜”
#### 2.7. 在右侧“场景视频滤镜”中，设置“图像格式”为“jpg”，“图像宽度”为“-1”，“图像高度”为“-1”，“文件名前缀”为空，“目录路径前缀”为图片要导出的目标目录（注意，每个视频的帧导出目标目录不同，千万不要设置错），不要勾选“总是写入到相同的文件中”，“录制比率”为“1”（1代表每帧都取，2代表隔帧取，以此类推），保存。
<img src="https://github.com/wangxizhe2017/XY_Cap_Endo_Dataset_Guide/blob/main/images/4.png" width="450">

#### 2.8. 每次运行一个视频前，先执行2.6. ～ 2.7.，设置对应的导出目录。保存设置后，播放视频，每帧图片就自动导出，且图片名会根据帧号自动生成。
#### 2.9. 注意，取帧图片时，保持视频正常速度播放，不要暂停、关闭、拖拽时间进度条等，直到视频播完。

