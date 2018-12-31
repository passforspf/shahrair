# shahrair
Project1
    int[][][] pieces = new int[][][] { { { 0, 0 }, { 1, 0 }, { 0, 1}, { 1, 1 } },
                                         { { 0, 0 }, { 0, 1 }, { 0, 2 }, { 0, 3 } },
                                         { { 0, 0 }, { 0, 1 }, { 0, 2 }, { 1, 2 } },
                                         { { 0, 0 }, { 0, 1 }, { 0, 2 }, { 1, 1 } },
                                         { { 0, 0 }, { 0, 1 }, { 1, 1 }, { 1, 2 } } };
                                         // couples are each figure's squares' (x,y) pos. stepping 40 pixels  

    RectangleShape square = new RectangleShape(new Vector2f(40, 40)); // figure's square, 40 pixels side

    private void DrawTetrisPiece(int x, int y, int index) // (x, y) is the position in the playing Box
    {
        int a;
        for (a = 0; a < 4; a++)
        {
            square.Position = new Vector2f(x + pieces[index][a][0] * 40, y + pieces[index][a][1] * 40);
            window.Draw(square);
        }
    }
