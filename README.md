# Check-Array-Formation-Through-Concatenation
class Solution:
    def canFormArray(self, arr: list[int], pieces: list[list[int]]) -> bool:
        if arr is None and pieces is None:
            return True
        if arr is None or pieces is None:
            return False
        r=[]
        for i in arr:
            for j in pieces:
                if i==j[0]:
                   r.extend(j)
                   break
        if r==arr:
           return True
        return False
