一个印度人实现的动作识别程序（包括表情和手势识别），基本算法就是把OpenPOSE跟踪出来的人体各关键点与第0号关键点（脖子）计算距离（欧拉或cos距离），然后所有点的距离形成的数组交给一个训练好的LSTM分类器模型进行推导，得出的结果就是判定的动作；LSTM模型是事先训练好的（GitHub上有训练和创建网络的python程序），模型里包括所有要推导的动作，所以要添加动作就要重新训练模型；
