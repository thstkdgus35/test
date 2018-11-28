# 1. pytorch
### AssertionError: nn criterions don’t compute the gradient w.r.t. targets - please mark these variables as volatile or not requiring gradients

  vgg 같은 네트워크를 활용해서 perceptual loss를 구할때 생기는 문제
  output, target = vggmodel(SR), vggmodel(HR)
  Loss = L2(output, target)
  target = target.detach()이 아니라 L2(output, target.detach())로 해결
  
### argparser의 string과 직접 입력한 string이 다른 문제
  a.find('b') > -1 이면 a안에 b

#### 주의
HR = HR.detach()로 하면 해결 
# 2. numpy

# 3. tensorflow
