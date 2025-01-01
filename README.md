# -6Companies30days
#include <iostream>
#include <cmath>

class Solution {
public:
    bool checkOverlap(int radius, int xCenter, int yCenter, int x1, int y1, int x2, int y2) {
        int xnearest = std::max(x1, std::min(xCenter, x2));
        int ynearest = std::max(y1, std::min(yCenter, y2));

        int dist = (xCenter - xnearest) * (xCenter - xnearest) + (yCenter - ynearest) * (yCenter - ynearest);

        return dist <= radius * radius;
    }
};

int main() {
    Solution sol; // Create an object of the Solution class
    bool result = sol.checkOverlap(4, 102, 50, 0, 0, 100, 100); // Call checkOverlap using the object
    std::cout << (result ? "Overlap" : "No Overlap") << std::endl; // Print result
    return 0;
}
