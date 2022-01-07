var medianSlidingWindow = function(nums, k) {
    if (!nums.length) {
        return [];
    }

    // find the median of the first window
    const firstSlided = nums.slice(0, k);

    let medians = [findMedian(firstSlided)];

    for (let i = k; i < nums.length; i++) {
        const slidedArr = nums.slice(i - k + 1, i + 1);
        medians.push(findMedian(slidedArr));
    }

    return medians;
};

const findMedian = (arr) => {
    // get copy of the original array
    const a = arr.slice();

    // should be SORTED
    a.sort((a, b) => a - b);

    const n = a.length;

    const middle = a[Math.floor(n / 2)];

    // ODD LENGTH
    if ((n & 1) !== 0) {
        return middle;
    } else {
        // EVEN LENGTH
        return (Math.floor(a[Math.floor((n - 1) / 2)] + middle) / 2);
    }
};
