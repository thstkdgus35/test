# 1. pytorch
### AssertionError: nn criterions don’t compute the gradient w.r.t. targets - please mark these variables as volatile or not requiring gradients

vgg 같은 네트워크를 활용해서 perceptual loss를 구할때 생기는 문제
output, target = vggmodel(SR), vggmodel(HR)
Loss = L2(output, target)
Loss = L2(vgg(output), vgg(target))과 같이 구하는데, output과 target 중 어느 이미지가 gradient를 요구하는 지 명시해줘야함

target = target.detach()로 해결 가능

#### 주의
HR = HR.detach()로 하면 해결 
# 2. numpy

# 3. tensorflow
