# pythone-score-grouping
def get_scores(arg_1):
    score_dict = {}
    for i in arg_1:
        pairs = i.split(":")
        key, value = pairs[0], int(pairs[1])
        if key in score_dict:
            score = score_dict[key]
            score_dict[key] = score + value
        else:
            score_dict[key] = value
    return score_dict



a = input().split(",")
result = get_scores(a)
result_1 = list(result.items())
result_1.sort()
print(result_1)
