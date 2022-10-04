# snakeprocession
new repo
ques=The annual snake festival is upon us, and all the snakes of the kingdom have gathered to participate in the procession. Chef has been tasked with reporting on the procession, and for this he decides to first keep track of all the snakes. When he sees a snake first, it'll be its Head, and hence he will mark a 'H'. The snakes are long, and when he sees the snake finally slither away, he'll mark a 'T' to denote its tail. In the time in between, when the snake is moving past him, or the time between one snake and the next snake, he marks with '.'s.

Because the snakes come in a procession, and one by one, a valid report would be something like "..H..T...HTH....T.", or "...", or "HT", whereas "T...H..H.T", "H..T..H", "H..H..T..T" would be invalid reports (See explanations at the bottom).
int main(void) {
{
    int t;
    scanf("%d", &t);
    for (int j = 0; j < t; j++)
    {
        int n;
        scanf("%d", &n);
        char snake[n];
        scanf("%s", snake);
        int h = 0, t = 0, i = 0;
        while (snake[i] != '\0')
        {
            if (snake[i] == 'H')
            {
                h++;
            }
            else if (snake[i] == 'T')
            {
                t++;
            }
            if (t > h || h > t + 1 || (i == (n - 1) && h > t))
            {
                printf("Invalid\n");
                break;
            }
            i++;
        }
        if (t == h)
        {
            printf("Valid\n");
        }
    }
}
	return 0;
}
