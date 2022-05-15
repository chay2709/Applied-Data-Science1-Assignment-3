def main():
    # filter indicator co2 emissions from main dataset
    co2_df = filter_co2_emissions()

    # apply kmeans for clustering the co2 emission data
    apply_kmeans(co2_df)

    # get a few years of data for aggregations
    agr_t_df = get_year_df()

    # plots curve fitting
    curve_fitting(agr_t_df)

    # compare curves exponent vs linear vs logistic
    compare_curves(agr_t_df)


if __name__=='__main__':
    main()
