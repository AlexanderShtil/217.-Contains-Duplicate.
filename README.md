# 217.-Contains-Duplicate.
#include <iostream>
#include <windows.h>
#include <string>
#include<unordered_map> 
#include <vector> 
class Solution {
public:
	std::vector<int> twoSum(std::vector<int>& nums, int target) {
		
		std::unordered_map<int, int > notebook;


		for (int i = 0; i < nums.size(); i++) {
			int current_num = nums[i];
			int required_num = target - current_num;

			if (notebook.count(required_num)) {
				return{ notebook[required_num], i };
			}

			notebook[current_num] = i;
		}
		return{};
	}
};

 int main(){
	 SetConsoleCP(1251);
	 SetConsoleOutputCP(1251);
	

	 return 0;
 }
