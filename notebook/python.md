[TOC]
# OS
| 模块/方法 | 作用 | 备注 |
|---|---|---|
| os.getcwd() | 返回当前工作目录 |  |
| os.listdir(path) | 列举指定目录中的文件名和目录名 |  |
| os.mkdir(path) | 创建单层目录 |  |
| os.makedirs(path,exist_ok=False) | 递归创建目录 |  |
| os.remove(path) | 删除文件 |  |
| os.rmdir(path) | 删除单层目录 |  |
| os.removedirs() | 递归删除目录 |  |
| os.rename(old,new) | 将老的文件名或目录重新命名为新的文件名或目录 |  |
| os.path.split(path)  | 将path分割成目录和文件名二元组返回 |  |
| os.path.dirname(path) | 返回path的目录 |  |
| os.path.basename(path)  | 回path最后的文件名 |  |
| os.path.exists(path)  | 如果path存在，返回True；如果path不存在，返回False |  |
| os.path.join(path1[, path2[, …]])  | 将多个路径组合后返回 |  |
| os.path.isdir()  | 是否为目录  |  |
| os.path.isfile()     | 是否为文件 |  |
# opencv
| 模块/方法 | 作用 | 备注 |
|---|---|---|
| cv2.imread(path，flag=1) | 读入path路径的图片 | cv.IMREAD_COLOR： 加载彩色图像。任何图像的透明度都会被忽视。它是默认标志。<br>cv.IMREAD_GRAYSCALE：以灰度模式加载图像  <br>cv.IMREAD_UNCHANGED：加载图像，包括alpha通道 <br>注意 除了这三个标志，你可以分别简单地传递整数1、0或-1。 读入后是BGR模式,<numpy.ndarray> |
| cv2.imwrite(path,img) | 保存图片 | 以BGR模式保存 |
| b,g,r = cv2.split(img) >>><br> img = cv2.merge((b,g,r)) | 拆分和合并通道 | 耗时，尽量用numpy索引 |
| cv2.copyMakeBorder(img,top，bottom，left，right,borderType,value) | 为图片填充边缘 | cv.BORDER_CONSTANT - 添加恒定的彩色边框。该值应作为下一个参数给出。<br>cv.BORDER_REFLECT - 边框将是边框元素的镜像，如下所示： <br>fedcba \| abcdefgh \| hgfedcb \|<br>cv.BORDER_REFLECT_101或 cv.BORDER_DEFAULT与上述相同，但略有变化，例如： gfedcb \| abcdefgh \| gfedcba \|<br>cv.BORDER_REPLICATE最后一个元素被复制，像这样： aaaaaa \| abcdefgh \| hhhhhhh \|<br>cv.BORDER_WRAP难以解释，它看起来像这样： cdefgh \| abcdefgh \| abcdefg \| value -边框的颜色，如果边框类型为cv.BORDER_CONSTANT |
| cv2.add(x,y) | 图像加法 |  |
| cv.addWeighted(x,0.7,y,0.3,0) | 图像融合 | 把x,y以0.7，0.3和gamma=0的偏移量相加 |
| cv2.cvtColor(img,flag) | 改变颜色空间 | flag有cv2.COLOR_BGR2RGB,cv2.COLOR_RGB2BGR，cv2.COLOR_BGR2GRAY |
| cv2.resize(img,Size,fx=0, fy=0,interpolation = INTER_LINEAR) | 改变图片尺寸 | 优先判断Size合不合法，如果不合法，则按fx，fy比例缩放 |
| cv2.bitwise_or(src, dst) |
| cv2.bitwise_and(src, dst) |
| cv2.bitwise_not(src) |
| cv2.bitwise_xor(src, dst) |  |  |
# matplotlib.pyplot
# shutil
| 模块/方法 | 作用 | 备注 |
|---|---|---|
| shutil.copyfile(src, dst) | 复制文件 |  |
| shutil.copy(src, dst) | 拷贝文件和权限 |  |
| shutil.rmtree(dir) | 递归的去删除文件 |  |
| shutil.move(src, dst) | 移动文件 |  |
# glob
| 模块/方法 | 作用 | 备注 |
|---|---|---|
| glob.glob(source) | 匹配满足条件的文件 | "glob.glob('dir/*') 星号(*)匹配零个或多个字符 |
| glob.glob('dir/file?.txt') 问号(?)匹配任何单个的字符  |
| glob.glob('dir/*[0-9].*') 匹配一个特定的字符，可以使用一个范围" |
