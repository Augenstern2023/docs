.. _cn_api_paddle_nn_functional_softplus:

softplus
-------------------------------

.. py:function:: paddle.nn.functional.softplus(x, beta=1, threshold=20, name=None)

softplus 激活层

.. math::
    softplus(x)=\begin{cases}
            \frac{1}{\beta} * \log(1 + e^{\beta * x}),&x\leqslant\frac{\varepsilon}{\beta};\\
            x,&x>\frac{\varepsilon}{\beta}.
        \end{cases}

其中，:math:`x` 为输入的 Tensor。

参数
::::::::::::

 - **x** (Tensor) - 输入的 ``Tensor``，数据类型为 float32 或 float64。
 - **beta** (float，可选) - Softplus 激活计算公式中的 :math:`\beta` 值。默认值为 1。
 - **threshold** (float，可选) - Softplus 激活计算公式中的 :math:`\varepsilon` 值。默认值为 20。
 - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

返回
::::::::::

    ``Tensor``，数据类型和形状同 :attr:`x` 一致。

代码示例
::::::::::

COPY-FROM: paddle.nn.functional.softplus
